---
title: '创建个人博客的记录'
date: 2022-10-28 20:51:57
tags: []
published: true
hideInList: false
feature: https://gitee.com/jiekeaoteman/blgimg/raw/master/img/NzAwODE0ODlfMTEyMTY2MTQ3NTI=_7.webp.jpg
isTop: false
---


## 一、 注册GitHub账号，建立仓库

* 参考链接： [如何在 GitHub 上写博客？](https://www.zhihu.com/question/20962496)   [GitHub Pages帮助页面](https://help.github.com/cn/github/working-with-github-pages)

* GitHub宣布，自2020年10月1日起，在GitHub平台上创建的所有源代码存储库都将默认命名为 main ，而非原本的 master  所以在一些老的教程会看到master

* 为什么取仓库名字为username.github.io？

  ![image-20201121104551018](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121104551018.png)

* 建立仓库后会选择主题，在我尝试使用jekyll主题后我发现我下载的主题还要进行一些文件的配置，我嫌麻烦就放弃了，也可能是我下载的主题自带了一些原主人的东西

* 接下来我去学习了git的使用以及下载了githubdesktop（后面没有使用，但是git是需要下载的）

  附我学习的视频连接[【2021年Git全集教程】大牛4小时带你精通Git玩转GitHub（最新版）](https://www.bilibili.com/video/BV1Zz4y1C7vg?p=1)

       笔记   链接：https://pan.baidu.com/s/1NZxaQOZPjJUcFQsSub0q-g   提取码：1c0y

## 二、 使用Gridea同步blog和PicGo上传图片

* 我是使用gitee仓库做的图床，github pages上发博客

  因为gitee是国内的所以访问速度会比github更加快一点，所以把图片资源放到gitee上去

  ps：我之前使用github的图床时使用picgo生成的链接没法用

  至于在github上发布blog是因为github受众广，稳定

* 注册一个gitee账号，建立仓库     [参考连接](https://gitee.com/help/articles/4169)

* [git安装地址](https://git-scm.com/downloads)      [gridea安装地址](https://gridea.dev/)  这个安装问题应该不大

### 配置Gridea

Gridea是一个静态的博客写作客户端，你可以在上面同步你的blog

接下来要进行一定的配置

![image-20201121115616587](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121115616587.png)

令牌获取：

![image-20201121144809276](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121144809276.png)

![image-20201121144852697](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121144852697.png)

![image-20201121144928730](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121144928730.png)

点击右上方的Generate new token，在Note输入对Token的描述或备注，勾选下方的repo生成即可。注意这个token只能看到这一次，最好记录下来。

将token输入令牌一栏后保存，点击远程连接测试，提示连接成功完成配置，失败则检查上面的配置信息

### 配置PicGo

要先下载最新版Node.js  [Node.js下载](https://nodejs.org/en/download/)  还需要npm（新版的Node.js中一般自带npm）

可以通过window终端输入`node -v` 和`npm -v`  看是否安装成功

下载PicGo   点击 [PicGo](https://picgo.github.io/PicGo-Doc/zh/guide/) 里面有帮助文档和下载

![image-20201121150736993](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121150736993.png)

打开PicGo在插件设置中搜索gitee（因为picgo软件未带上传gitee的部分需要下载插件）

![image-20201121150936036](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121150936036.png)

安装gitee-uploader，安装好了以后重启，打开图床设置中的gitee

![image-20201121151807061](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121151807061.png)

设为默认图床

获取gitee的token方法跟github差不多：设置->私人令牌->生成新令牌即可

此时可以在上传区上图片试试了，上传后应该打开gitee仓库就能看到图片文件



## 三、 使用Typora写博文，图片插入即时上传并生成连接

* 下载新版Typora（一些老版的没有图片上传功能），安装很简单。    [Typora下载](https://typora.io/)
* md语法基本看上不到10分钟就能会，可自行百度
* 文件->偏好设置->图像
* 文件->偏好设置->图像

![image-20201121155207168](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121155207168.png)

这样你可以在写文章时直接把图片粘贴进来，他会自动上传至gitee，并且生成连接

（其实gridea内置了编辑器，但是我觉得没有typora好用）

写完文章我一般都是将Typora中的内容复制到Gridea中去，使用Gridea来生成文章。因为一些头文件的规范直接放在源文件的posts中可能导致gridea解析出错，然后预览，没问题同步即可。

## 四、 Gridea主题

### 下载并更换主题 

[主题市场](https://gridea.dev/themes) 选择一个自己喜欢的主题下载

![image-20201121161611089](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121161611089.png)

点击下找到站点源文件，将下载的主题文件夹（下载的东西可能还有一些帮助文档啥的）放到站点源文件的themes里就好了，之后预览，同步，打开博客时可能会出现混乱，可以尝试Ctrl+F5刷新

tips：

F5刷新按钮只对当前页面进行刷新，只刷新本地缓存；

Ctrl + F5 的行为也是刷新页面，但是会把浏览器中的临时文件夹的文件删除再重新从服务器下载。
比如某网站更新了 style.css 文件，如果单纯按 F5 刷新，那么当前页面还是使用未修改的 style.css 文件内容，如果按 Ctrl + F5 就会重新从服务器下载 style.css 文件，并使用修改后的 style.css 文件。



### 主题的一些其他配置（以我下载的Fog主题为例）

* Valine评论配置

​        已注册lencloud  已使用npm下载Valine   ------>未完成

​        npm安装过慢使用淘宝服务器下载   以下载jquery为例    

​        `npm install jquery --registry=https://registry.npm.taobao.org`    

​        或者执行这行命令， npm 会从淘宝镜像下载包了，速度会比原来快很多 

​        `npm config set -g registry https:*//registry.npm.taobao.org* `

* 更换看板娘  ------> 未完成

* 文章热度一 直loding  查看主题帮助文档得：进入leancloud项目下，查看 部署-结构化数据 是否有Counter

​        如果没有，创建一个新的Class，名称为Counter------>未完成

----

---

上面部分基本已经搭建起来了个人博客，实现了更新文章等基本功能

下面是我想要 双线部署博客到到 Coding Pages 和 GitHub Pages 这需要一个自己的域名（可以阿里云腾讯云上花几块钱买一个便宜的域名）不买域名也可以将你的博客再部署到coding的静态网站上（毕竟国内访问速度快）

## 五、 部署blog到coding

注册coding账号，因为coding取消了个人版，所以要先创建一个团队，团队名根据自己起一个就行![image-20201121170914469](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121170914469.png)

![image-20201121171235012](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121171235012.png)

选择创建代码托管项目---->填好项目名称会自动生成项目标识---->完成创建

![image-20201121171552758](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121171552758.png)

点击左下角的项目设置![image-20201121181331328](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121181331328.png)

在项目设置 > 项目与成员 > 功能开关内打开持续集成，持续部署

![image-20201121181604295](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121181604295.png)

在左边持续部署中选择静态网站 > 创建静态网站   节点选择香港在绑定域名时可以不用备案

![image-20201121181852007](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121181852007.png)

在这你可以看到静态网站的地址

![image-20201121183414215](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121183414215.png)

获取coding 的token   之后勾选project:depot权限完成 （注意保存token，他之后没有办法查看忘了只能重新建立）

![image-20201121182449908](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121182449908.png)

完成以后再打开Gridea点击远程  > 进行coding pages的配置

![image-20201121183844678](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121183844678.png)

远程连接检测 > 同步即可    之后就可以打开之前静态网站的地址看一下自己的blog了

##  六、 双线部署博客到到 Coding Pages 和 GitHub Pages

标题的意思是通过一个域名分别绑定Coding和GitHub，在dns解析时设置国内ip访问域名时转到Coding国外ip访问域名时转到GitHub。不过我最后没有完成，因为Coding Pages从旧版更新以后如果要绑定自定义域名就必须使用腾讯云的cdn加速，这个项目是要收费的，所以我最终没有实现双线部署。就只绑定了GitHub Pages

* 域名绑定GitHub Pages

  进入仓库，选择Setting

  ![image-20201121194948373](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121194948373.png)

  然后下拉找到GitHub Pages里的Custom domain

  ![image-20201121195327094](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121195327094.png)

  之后他应该会自动生成一个CNAME（大写）的文件里面应该有你的域名，如果没有请自行创建并填写域名。

  ![image-20201121195639379](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121195639379.png)

  在Gridea的远程配置中CNAME添加自己的域名，不然每次同步后Github Pages的Custom domain会消失，接下来你就没法通过域名访问博客了

  新注册了一个域名后,并无法直接使用,而要访问网络上的服务器,必须通过服务器的IP，因此接下来要进行DNS解析。

  因为我是在腾讯云买的域名因此我以在腾讯云解析为例

  

![image-20201121201259936](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121201259936.png)

主机记录：一般选@就可以本来我的一个地址是https://xxxxxxx.com如果主机记录为@那么记录值选择xxxxxx.com就可以了

![image-20201121201359980](https://gitee.com/jiekeaoteman/blgimg/raw/master/img/image-20201121201359980.png)

TTL：  Time To Live  这个值越大修改解析后等待生效的时间越长，但是不能设置的太小，太小了域名解析的稳定性和解析速度收到影响

默认即可  600为600秒。添加上就可以通过你的域名访问你的博客了。

这里解释一下DNS解析是让你的域名可以找到你博客的地址，而想要让你的博客接受你这个域名的访问就必须进行添加CNAME