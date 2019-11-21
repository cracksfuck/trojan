# trojan
最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7


最简单的Trojan一键脚本，效率高/速度快/延迟低，系统>=Centos7，完美支持tls1.3，个人体验速度和延迟都优于v2ray+ws+tls1.3，本次的centos版使用了官方编译的二进制文件，搭建非常快速和简单。脚本中集成了Trojan的Windows客户端，自动配置证书及启动脚本，安装完成直接下载客户端即可。
系统要求及脚本介绍

1、系统>=centos7，用centos8最好，内核可直接开启bbr不需升级。

2、域名解析到VPS并生效。

3、脚本自动续签https证书

4、自动配置伪装网站，位于/usr/share/nginx/html/目录下，可自行替换其中内容
一、使用一键脚本安装

    curl -O https://raw.githubusercontent.com/atrandys/trojan/master/trojan_centos7.sh && chmod +x trojan_centos7.sh && ./trojan_centos7.sh

另外建议安装bbr，以下脚本安装，不赘述了

    cd /usr/src && wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh

二、下载Windows客户端

安装完成后，会展示一条下载地址，复制地址，并下载下来即可。
三、搭配浏览器插件使用

解压缩下载的trojan-cli.zip的压缩包，进入文件夹，双击start.bat，开启Trojan服务，Trojan会监听本地1080端口。然后下载switchomega

    下载插件：switchyomega

安装插件，打开chrome，打开扩展程序，将下载的插件拖动到扩展程序页面，添加到扩展。

最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7

完成添加，会跳转到switchyomega页面，点跳过教程，然后点击proxy，如图填写，最后点击应用选项。

最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7

然后进入auto switch，删除最上方两条规则，然后点击添加规则列表。

最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7

然后，在规则列表规则中，情景模式改为proxy，规则列表网站复制下面的网址，然后点击立即更新情景模式，保存即可。

    https://raw.githubusercontent.com/atrandys/proV/master/fgfwlist.txt

最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7

点击chrome右上角switchyomega图标，选择auto switch模式即可。

最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7

之后你便可以自由上网，教程到此结束。
电脑上其他软件如何使用Trojan

    1、如果软件支持配置socks5，直接指向127.0.0.1：1080即可。

    2、如果软件不支持配置socks5，可选择sstap/sockscap64/supercap等软件，曲线实现代理。

常见问题总结

1、Trojan客户端打开无法运行，提示缺少找不到vcruntime140.dll或找不到msvcp140.dll。

    原因缺少运行库，点击下载链接中的两个软件，一个是32位一个是64位，请全部安装即可。

2、如果遇到vcruntime140_1的错误，下载下面的文件放到C:\windows\system32目录下即可

点击下载140_1.dll
文章标题：最简单的Trojan一键脚本，效率高/速度快/延迟低，支持tls1.3，系统要求>=Centos7
固定链接：https://www.atrandys.com/2019/1963.html
转载。 
