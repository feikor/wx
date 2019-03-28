# wx
微信开发


名词备注：

authorization_code                #授权码

query_auth_code                   #查询身份验证代码

component_verify_ticket           #组件验证票


第三方平台
1.获取微信平台推送的组件验证票据（component_verify_ticket）
component_verify_ticket           #微信服务器每隔10分钟会向第三方的消息接收地址推送一次component_verify_ticket，用于获取第三方平台接口调用凭据
2.获取第三方平台自己的组件访问令牌(component_access_token)
component_access_token            #第三方平台通过自己的component_appid（即在微信开放平台管理中心的第三方平台详情页中的AppID和AppSecret）和component_appsecret，以及component_verify_ticket（每10分钟推送一次的安全ticket）来获取自己的接口调用凭据（component_access_token)
3.获取预授权码(pre_auth_code)
获取预授权码pre_auth_code          #第三方平台通过自己的接口调用凭据（component_access_token）来获取用于授权流程准备的预授权码（pre_auth_code）
4使用授权码换取公众号或小程序的接口调用凭据和授权信息(授权人访问令牌authorizer_access_token)
authorizer_access_token          #通过授权码和自己的接口调用凭据（component_access_token），换取公众号或小程序的接口调用凭据（authorizer_access_token和用于前者快过期时用来刷新它的authorizer_refresh_token）和授权信息（授权了哪些权限等信息）
