#### Serverless 

Serverless 是最近几年业界很火的技术名词，你可以在国内外各种技术大会上看到它的身影，主流云服务商也不断地推出 Serverless 相关的云产品和新功能（比如 AWS Lambda、阿里云函数计算、腾讯云云函数），各种关于 Serverless 的商业和开源产品也层出不穷（比如 Serverless Framework、OpenFaaS、kubeless）。

在这个背景下，开始使用 Serverless 的产品，用它来解决实际问题，比如用 Serverless 技术实现自动化运维、开发小程序、开发服务端应用。

但是我们是否思考过 Serverless 为什么这么火呢，换句话说，Serverless 架构兴起的必然因素是什么？

在说到Serverless之前，就不得不说云计算，因为云计算的发展史就是 Serverless 的兴起史。

纵观云计算的历史，我们可以将其分为物理机时代、虚拟机时代、容器时代、Serverless 时代，所以接下来，就让我们深入云计算的发展史，去寻找 Serverless 架构兴起的必然因素。

#### 物理机时代

<p align="center">
<img width="500" align="center" src="../images/181.jpg" />
</p>

但是对于云计算的概念其实可以追溯到 60 多年前，最早的说法是图中的“分时操作系统”，也就是通过时间片轮转的方式把一个操作系统给多个用户使用。同时还在发展的是虚拟化技术，也就是把一台物理机隔离为多台虚拟机，这样就能把一个硬件给多个用户使用。

1997 年，Ramnath Chellapa 教授把云计算定义成“一种新的计算范式，其中计算的边界将由经济原理决定，而不仅仅是技术限制”，通俗来讲就是，云计算不只是虚拟化技术，还是云服务商提供计算资源，使用者购买计算资源。

总的来说，在 2000 年之前，互联网刚刚兴起，而云计算还处于理论阶段，也就是物理机时代。如果这个时候你想在创业，开发一个电商网站，上线就需要经过以下步骤：

* 购买一台服务器（物理机）；

* 找个机房并给服务器通上电、连上网线；

* 在服务器上安装操作系统；

* 在服务器上安装数据库和网站环境；

* 部署网站；

* 测试；

这时你的网站架构是单机版的单体架构，数据库、应用、Nginx 等服务全都在一台你自己管理的服务器上。

网站上线之后，你将会遇到各种各样的问题，一旦停电，就会导致网络中断，服务器也会停机，那网站就没办法访问了，因此呢，用户不能再不断去买。于是为了避免断电、断网，大概率会选择把服务器托管到电信机房，那里停电的概率低很多，但是每个月得多付一些租金。

但是没想到半年后，问题又出现了，服务器 CPU 烧毁了！这不是简单换一台服务器就能解决的事情，原来服务器上的数据如何迁移？新的环境如何与原来保持一致？怎么保证网站持续可用，各种问题接连而至......

总的来说，物理机时代，网站上线和稳定运行面临的最大问题就是服务器等硬件问题，你既要购买服务器，还要承担服务器的场地、电力、网络等开销，并且还需负责服务器的维护。好在随后几年随着虚拟化技术逐渐成熟，云计算逐渐进入虚拟机时代，这也给我们带来了希望。

#### 虚拟机时代

<p align="center">
<img width="500" align="center" src="../images/182.jpg" />
</p>