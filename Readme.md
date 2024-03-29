# 渗透环境

## 工作环境

* 工作时全部操作均在虚拟机中完成
* 虚拟机中不登陆个人帐号，如QQ、微信、网盘、CSDN等
* 渗透环境、开发环境、调试环境需要分开，从目标服务器上下载的程序需要在单独的环境中测试运行
* 渗透虚拟机中全程使用代理IP上网
* 物理机必须安装安全防护软件，并安装最新补丁，卸载与公司相关的特定软件
* fofa、cmd5、天眼查等第三方工具平台帐号密码不得与公司有关，云协作平台同理
* RAT使用CDN保护的域名上线
* 尽量不使用公司网络出口，可以使用移动4G网卡，然后虚拟机再连代理
* 项目结束之后，虚拟机恢复快照，并且不再复测之前的目标或之前未成功利用的漏洞
* 工作记录使用mybase等加密记录，不使用在线文档，本地word等

## 渗透工具

* WebShell不能使用普通一句话木马，连接端使用加密流量，建议使用蚁剑
* 不使用默认冰蝎，需要修改为硬编码密钥
* 内网渗透时尽量使用socks代理，在本地操作
* 上传程序到目标服务器时，需要修改文件名：如svchost等，尽量不上传内部自研工具
* 公开工具需要去除特征指纹，如：sqlmap、masscan、Beacon证书
* 工具需要设置线程或访问频率，如sqlmap的--delay、内网扫描时线程不大于5
* Cobalt Strike后⻔上线后，设置time.sleep⼤于500秒
* 手机短信验证码需使用在线平台如z-sms.com，(中国移动可以申请和多号，然后设置只接收短信不接收电话)
* socks代理通道需要使用SSL加密
* 禁止在CS服务器上开启web服务，特别是在home目录
* 小范围流传的工具建议各大微信群公开，以免被人上传后被意外溯源，而你正好又是参演队伍
* 木马编译环境中用户名使用administrator，禁止使用自己的ID
* 自建dnslog平台的whois信息需要隐藏
* 自研扫描器不要带有特征，常见于user-agent处

## 重点

* 攻防演习成功的关键是团队协作，要互相帮助学习和进步，不要勾心斗角，每个团队的成功都需要有人当红花有人当绿叶的，外网打点与内网渗透同等重要
* 渗透过程中，记住上传的webshell、木马等地址，服务器添加的帐号，项目结束后要删除或描述在报告中，避免不必要的麻烦
* 登陆3389不建议添加用户，尝试激活guest，如必须要添加帐户，帐户名与目标相关即可，避免使用qax、qaxNB等友商关键词
* 清理日志时需要以文件覆盖的方式删除文件，防止数据恢复，或者仅删除指定ID的日志
* 碰到蜜罐就不要慌，多喝点花茶，这样死了会比较香



