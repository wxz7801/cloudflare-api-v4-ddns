Cloudflare API v4 Dynamic DNS Update in Bash, without unnecessary requests
Now the script also supports v6(AAAA DDNS Recoards)

魔改了一些部分，当前功能为从多个源域名获取ip并解析到对应的目标域名上。

----

创建 Cloudflare API 令牌，请转到 https://dash.cloudflare.com/profile/api-tokens 并按照以下步骤操作：

1. 单击创建令牌
2. 为令牌提供一个名称，例如，`cloudflare-ddns`
3. 授予令牌以下权限：
    * 区域 - 区域 - 读取
    * 区域 - 区域设置 - 读取
    * 区域 - DNS - 编辑
4. 将区域资源设置为：
    * 包括 - 特定区域 - 选择你想设置的域名

----
![image.png](https://i.loli.net/2021/11/13/OMpjhUyubrwN6Lk.png)

需要在脚本内定义多个原域名和目标域名
