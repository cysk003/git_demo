    四季線上 4GTV 免费播放全部频道 第三弹 🥚🥚🥚 · pixman.io               

[![Logo](https://assets.pixman.io/site/icon-128.png)](/)

[

IPTV 四季線上 4GTV 免费播放全部频道 第三弹 🥚🥚🥚
==================================

](# "四季線上 4GTV 免费播放全部频道 第三弹 🥚🥚🥚")

*   [首页](/)
*   [热门](/topics/popular)
*   [精华](/topics/excellent)
*   [新发布](/topics/last)
*   [新回复](/topics/last_reply)

*   [注册](/account/sign_up)
*   [登录](/account/sign_in)

[IPTV](/topics/node2) 四季線上 4GTV 免费播放全部频道 第三弹 🥚🥚🥚
===================================================

[coding](/coding) · 2024年05月18日 · 最后由 [qinsmoon](/qinsmoon) 回复于 2024年05月18日 · 331 次阅读

[![](https://assets.pixman.io/user/avatar/1/49018a.png?x-oss-process=image%2Fresize%2Cw_96%2Ch_96%2Cm_fill)](/coding "coding (Coding)")

本帖已被管理员设置为精华贴

前面两🥚已经分享了代码原理和镜像使用方法，这次我完善了频道列表和 logo，以及匹配了 EPG 信息，同时新增了以下频道：

*   4gtv-4gtv066 台視
*   4gtv-4gtv051 台視新聞
*   4gtv-4gtv056 台視財經台
*   4gtv-4gtv104 第 1 商業台
*   litv-longturn01 龍華卡通台
*   litv-longturn12 龍華偶像台
*   litv-longturn21 龍華經典台
*   litv-longturn19 Smart 知識台
*   litv-longturn22 台灣戲劇台
*   4gtv-4gtv010 非凡新聞台
*   litv-longturn04 博斯魅力台
*   litv-longturn06 博斯高球二台
*   litv-longturn08 博斯運動二台
*   litv-longturn13 博斯無限二台

使用
--

首先你需要在服务器或者电脑上安装 Docker，安装方法：[https://docs.docker.com/engine/install/](https://docs.docker.com/engine/install/)，然后使用 `docker pull pixman/4gtv` 拉取最新镜像。

在启动容器之前，你需要确保你的网络没有问题，如果是以下情况，则可以直接运行 `docker run --name=4gtv -d -p 5000:5000 pixman/4gtv` 来启动容器。

*   服务器或设备位于中国大陆以外的地区
*   服务器或设备已经将网关指向了旁路由或者其他设备上的代理软件
*   服务器或设备上游网络已经配置了代理软件

如果你的情况不符合上述条件，你需要在运行容器时设置环境变量，如下：

    docker run --name=4gtv -d -p 5000:5000 -e HTTP_PROXY=http://192.168.1.1:7890 -e HTTPS_PROXY=http://192.168.1.1:7890 pixman/4gtv
    

请注意将 `192.168.1.1:7890` 替换为你的代理软件的地址和端口，如果你的代理软件是 Openclash，也许还需要配置代理所需的用户名和密码，将上面的命令改为：

    docker run --name=4gtv -d -p 5000:5000 -e HTTP_PROXY=http://user:[email protected]:7890 -e HTTPS_PROXY=http://user:[email protected]:7890 pixman/4gtv
    

在启动容器之后，可以访问 `http://127.0.0.1:5000/4gtv.m3u` 来获取频道列表，访问 `http://127.0.0.1:5000/4gtv/{ID}` 来播放某个频道。

对于普通用户来说，上述步骤就是足够了，假如你配置了反向代理，那么获取频道列表的时候需要额外的 domain 参数，例如 `http://127.0.0.1:5000/4gtv.m3u?domain=http%3A%2F%2Fexample.com`，这样可以确保播放地址是正确的。

![](https://assets.pixman.io/photo/coding/2746d913-6208-49cc-97b6-aa4637b665f3.png?x-oss-process=image%2Fresize%2Cw_1920)

[6 个赞](# "赞")

[](#)

[![](https://assets.pixman.io/user/avatar/1/49018a.png?x-oss-process=image%2Fresize%2Cw_32%2Ch_32%2Cm_fill)](/coding "coding (Coding)") [coding](/coding) 将本帖设为了精华贴。 05月18日 01:44

[![](https://pixman.io/system/letter_avatars/h.png)](/huanxian "huanxian (小白)")

[huanxian](/huanxian) #2 [2024年05月18日](#reply-153)

好评

[](# "回复此楼")[](/topics/13/replies/153/edit "修改")

[](# "赞")

[![](https://assets.pixman.io/user/avatar/13/d381b6.jpg?x-oss-process=image%2Fresize%2Cw_96%2Ch_96%2Cm_fill)](/YuanKong "YuanKong (圆空)")

[YuanKong](/YuanKong) #3 [2024年05月18日](#reply-158)

太强了，三连![👍](https://twemoji.ruby-china.com/2/svg/1f44d.svg ":+1:") ![👍](https://twemoji.ruby-china.com/2/svg/1f44d.svg ":+1:") ![👍](https://twemoji.ruby-china.com/2/svg/1f44d.svg ":+1:")

[](# "回复此楼")[](/topics/13/replies/158/edit "修改")

[](# "赞")

[![](https://pixman.io/system/letter_avatars/q.png)](/qinsmoon "qinsmoon (qinsmoon)")

[qinsmoon](/qinsmoon) #4 [2024年05月18日](#reply-159)

👍👍👍

[](# "回复此楼")[](/topics/13/replies/159/edit "修改")

[](# "赞")

需要 [登录](/account/sign_in) 后方可回复, 如果你还没有账号请 [注册新账号](/account/sign_up)

[![](https://assets.pixman.io/user/avatar/1/49018a.png?x-oss-process=image%2Fresize%2Cw_96%2Ch_96%2Cm_fill)](/coding "coding (Coding)")

[

Coding

@coding

](/coding)

* * *

Just coding ...

* * *

[6 个赞](# "赞")

* * *

[](# "分享到 Twitter")[](# "分享到 新浪微博")[](# "分享到 Facebook")[](# "分享到 微信")

* * *

共收到 **3** 条回复

[

收到新回复，点击立即加载](#)

![pixman.io](https://assets.pixman.io/site/icon-256.png)

由 Pixer 共同维护的数字生活交流社区，本站使用 [homeland](https://github.com/ruby-china/homeland) 构建，并采用 [Docker](https://www.docker.com/) 部署

本网站服务器由 [![oracle](https://assets.pixman.io/site/oracle.svg)](https://www.oracle.com/cloud/ "本站服务器由 Oracle Cloud 提供") 提供， CDN 由 [![cloudflare](https://assets.pixman.io/site/cloudflare.svg)](https://www.cloudflare.com/ "CDN 由 Cloudflare 提供") 提供

App.root\_url = "https://pixman.io/"; App.asset\_url = "https://assets.pixman.io"; App.twemoji\_url = "https://twemoji.ruby-china.com/2"; App.locale = "zh-CN"; Topics.topic\_id = 13; $(document).ready(function(){ $.post("/topics/13/read"); }) ga('create', 'G-FBSY0WYMSC', 'auto'); ga('require', 'displayfeatures'); ga('send', 'pageview');