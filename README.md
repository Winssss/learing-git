## 1.Git的基础
### 1.1 Git的介绍

Git是目前世界上最最先进的分布式版本控制系统。

版本控制系统:
设计师在设计的时候做了很多版本

![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230ab67d48c2?w=325&h=210&f=png&s=52747)

经过了数天去问设计师每个版本都改了些啥，设计师此时可能就说不上来了。此时如果有一个软件能够能够记录每次的文件改动，并且还能协调多用户编辑，那岂不是美哉？这个软件应用起来应该像这个样子：
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230abb5a2dd0?w=649&h=137&f=png&s=51259)
### 1.2 Git与Github
#### 1.2.1 两者区别
Git是一个分布式版本控制系统，__简单的说其就是一个软件__，用于记录一个或若干文件内容变化，以便将来来查阅特定版本修订情况的软件

Github（https://www.github.com）是一个为用户提供Git服务的网站，简单说就是一个可以放代码的地方（不过可以放的当然不仅是代码）。Github除了提供管理Git的web界面外，还提供了订阅、关注、讨论组、在线编辑器等丰富的功能。Github被称之为**全球最大的基友网站**。

#### 1.2.2 Github注册
打开Github官网：https://www.github.com，点击右上角的“Sign up”按钮。

 1. 填写注册账号信息

![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230ab8dd0e64?w=633&h=784&f=png&s=60988)

 2. 完成邮箱验证
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230abc171906?w=925&h=363&f=png&s=59479)
#### 1.3 Git安装
 
1. 打开下载网站 [https://git-scm.com/downloads](https://git-scm.com/downloads)

2. 根据自己的操作系统选择对应的版本
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230abe27286e?w=706&h=659&f=png&s=143517)
3. 选择好安装路径后，一路按Next即可
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230abe5c7b81?w=444&h=363&f=png&s=112362)
4. 安装完成，点击右键，如有红框内容即安装成功
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230ae67adf71?w=219&h=354&f=png&s=16271)


## 2.Git的使用
### 2.1 本地仓库
#### 2.1.1 工作流程
Git本地操作的三个区域：
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230af0992306?w=461&h=253&f=png&s=77881)
工作流程：
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230aee78f767?w=548&h=275&f=png&s=88079)
### 2.2 本地仓库操作
 什么是仓库呢？仓库又名版本库，英文名repository，我们可以简单理解成是一个目录，用于存放代码的，这个目录里卖弄的所有文件都可以被Git管理起来，每个文件的修改、删除等操作Git都能跟踪到。

 1. 在安装后首次使用需要先进行全局配置
桌面空白处右键，点击“Git Bash Here”以打开Git命令行窗口
	```
	$git config --global user.name "用户名"
	$git config --global user.email "邮箱地址"
	```
 2. 创建仓库
 当我们需要让Git去管理某个新项目/已存在项目的时候，就需要创建仓库了。注意：目录名不能包含中文。
 	a. 创建空仓库
 						![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230af0f77cb5?w=606&h=393&f=png&s=25640)
   b. 在命令行中进入项目目录git-demo
 		![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230af3bf8f97?w=440&h=91&f=png&s=7211)
   c. Git仓库初始化（让Git知道，它需要来管理这个目录）
   		指令：git init
		![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230afecb5504?w=678&h=78&f=png&s=8420)
		**表现：执行之后会在项目目录下创建“.git”的隐藏目录，这个目录是git所创建，不能删除，也不能随意更改其中的内容。**

 3. Git常用指令操作
查看当前状态：git status        
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b1586acd0?w=505&h=199&f=png&s=15045)
添加到缓存区：git add 文件名
	```
	说明：git add指令，可以添加一个文件，也可以同时添加多个文件。
	语法 1：git add 文件名
	语法 2：git add 文件名 1 文件 2 文件 3 ...
	语法 3： git add .            [添加当前目录里所有文件到缓存区]
	```
	![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b1db9dc5a?w=482&h=241&f=png&s=31644)
提交至版本库：git commit -m "注释内容"
![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b2102fe04?w=463&h=86&f=png&s=8767)
### 2.3 版本回退
版本回退分为两步骤进行操作：
步骤:
	
 1. 查看版本，确定需要回到的时刻点
 		
    指令：
 		git log   --- 详细显示版本信息
 	    ![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b25c420d1?w=462&h=200&f=png&s=35075)
    	git log --oneline 或者 git log --pretty=oneline        --- 简略显示版本信息
    	![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b29449b38?w=533&h=191&f=png&s=20964)

 2. 回退操作
 		指令： git reset --hard 版本号

    举个栗子：
    
    文件夹原本包含有2个文件
    ![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b2a67ecc0?w=613&h=147&f=png&s=15530)
    执行命令后，版本号回退到最开始的时候
    ![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b42fd70f9?w=593&h=176&f=png&s=21744)
    
    **注意：回退过去之后，如果想再回到原本最新的版本的时候，则需要使用指令去查看历史操作，
    以得到最新的commit id。**
    
    指令：git reflog
    ![在这里插入图片描述](https://user-gold-cdn.xitu.io/2020/4/16/1718230b50a3c488?w=623&h=134&f=png&s=20959)
    
    小结：
	
	a. 要想回到过去，必须得到commit id, 然后通过 git reset --hard 进行回退；
	
	b. 要想回到未来，需要使用git reflog 进行历史操作查看， 得到最新的commit id;
	
	c. 在写回退指令的时候commit id 可以不用写全，git 自动识别，但是也不能写太少，至少需要写前4位字符。
	
### 2.2 远程仓库
 已github为例

1. 首先点击左上方Repositories里的New按钮
    
![](https://user-gold-cdn.xitu.io/2020/4/16/171823b5f0c1578d?w=324&h=111&f=png&s=4164)
2. 然后进入仓库创建页面

![](https://user-gold-cdn.xitu.io/2020/4/16/171823e89d52f8c7?w=718&h=651&f=png&s=54728)

3. 仓库创建成功

![](https://user-gold-cdn.xitu.io/2020/4/16/171823f37ef0c26d?w=1012&h=794&f=png&s=81150)

### 2.3 两种常规使用方式

#### 2.3.1 基于http协议
1.  使用clone 指令克隆线上仓库到本地
    
    语法：git clone 线上仓库地

    ![](https://user-gold-cdn.xitu.io/2020/4/16/1718244fdea56489?w=952&h=110&f=png&s=19020)
    ![](https://user-gold-cdn.xitu.io/2020/4/16/17182488e64de817?w=435&h=131&f=png&s=10069)

2. 在仓库上做对应的操作（提交暂存区、提交本地仓库、提交线上仓库、拉取线上仓库）
    
    提交到线上仓库的指令： git push
    
    ![](https://user-gold-cdn.xitu.io/2020/4/16/171824fe381ed44f?w=461&h=128&f=png&s=12133)
    
    
    ![](https://user-gold-cdn.xitu.io/2020/4/16/1718252dbcfacdfb?w=1006&h=446&f=png&s=47542)
    
    拉取线上仓库：git pull
    
![](https://user-gold-cdn.xitu.io/2020/4/16/17182575555e7b95?w=603&h=184&f=png&s=17350)

#### 2.3.2 基于ssh协议

**该方式与前面https方式相比，只是影响github对于用户的身份鉴权方式，对于git的具体操作（如提交本地、添加注释、提交远程等操作）没有任何影响。**

生成公私钥对指令（需要安装OpenSSH）:ssh-keygen -t rsa -C "注册邮箱"

步骤：
    1. 生成客户端公私钥文件
    2. 将公钥上传到Github

实际操作：
1. 打开提示
![](https://user-gold-cdn.xitu.io/2020/4/16/1718264be978a980?w=365&h=300&f=png&s=18413)

2. 创建公私钥对文件

![](https://user-gold-cdn.xitu.io/2020/4/16/171826844c859593?w=467&h=283&f=png&s=17049)
 
3. 上传公钥文件内容（id_rsa.pub）

![](https://user-gold-cdn.xitu.io/2020/4/16/171826bd765c0410?w=763&h=423&f=png&s=38011)

填写完毕后，保存即可

4. 执行后续git操作，操作与http协议一样
    
    a. 将线上仓库克隆到本地 （git clone）
        ![](https://user-gold-cdn.xitu.io/2020/4/16/17182710c65dd286?w=793&h=209&f=png&s=32728)

    b. 添加文件到线上仓库
        ![](https://user-gold-cdn.xitu.io/2020/4/16/17182750b4f742a5?w=757&h=285&f=png&s=38207)
        效果：
        ![](https://user-gold-cdn.xitu.io/2020/4/16/1718276c53ba53b1?w=990&h=157&f=png&s=15373)
        
#### 2.4 分支管理

什么是分支？

分支就是项目里的每个模块或者每个功能

![](https://user-gold-cdn.xitu.io/2020/4/17/171861b498bcf5c2?w=739&h=581&f=png&s=128154)

每次提交提交后都会有记录，Gi把塔曼串成事件线，形成类似于时间轴的东西，这个时间轴就是一个分支，我们之为**master分支**。

在开发的时候往往是团队写作，多人进行开发，因此光有一个分支是无法满足多人同时开发的需求的，并且在分支上工作并不影响其他分支的正常使用，会更加安全，Git鼓励开发者使用分支去完成一些开发任务。
    
    分支相关指令：
    查看分支：git branch
    创建分支: git branch 分支名
    切换分支: git checkout 分支名
    删除分支：git brance -d 分支名
    合并分支：git merge 被合并的分支名

查看分支：
![](https://user-gold-cdn.xitu.io/2020/4/17/171862a86134c951?w=572&h=79&f=png&s=6542)
注意： 当前分支前面哟古额标记“*”。

创建分支：

![](https://user-gold-cdn.xitu.io/2020/4/17/171862bdf418077a?w=587&h=118&f=png&s=10230)

切换分支：

![](https://user-gold-cdn.xitu.io/2020/4/17/171862d4520685d2?w=588&h=126&f=png&s=11469)

合并分支：

首先在dev分支下的readme文件新增一行并提交本地

![](https://user-gold-cdn.xitu.io/2020/4/17/171863b14ed34353?w=813&h=171&f=png&s=27662)

切到到master 分支下观察readme文件

![](https://user-gold-cdn.xitu.io/2020/4/17/171863d33413af80?w=766&h=139&f=png&s=19088)

将dev分支的内容与master分支合并

![](https://user-gold-cdn.xitu.io/2020/4/17/171863f1ad17fdc1?w=827&h=152&f=png&s=21260)

删除分支：

![](https://user-gold-cdn.xitu.io/2020/4/17/17186403f1f26170?w=588&h=117&f=png&s=11377)

**注意：在删除分支的时候，一定要先退出要删除的分支，否则删除不了。**


合并所有分支之后，需将master保存到远程仓库

![](https://user-gold-cdn.xitu.io/2020/4/17/1718644571b971b2?w=975&h=188&f=png&s=27597)

## 3.Git使用技能

