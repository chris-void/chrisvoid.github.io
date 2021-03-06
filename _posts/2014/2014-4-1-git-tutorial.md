---
layout: post
title: Git Tutorial
description: 在Git流行的时代,入门
category: blog
---

# Pro Git

### git cheatsheet

**git status**

```sh
$ git status -s
$ git diff --stat
$ git diff --cached --stat
$ git diff HEAD --stat
```




## What is Git / Github

### Git/Github的产生

对于大部分人来说,Git的大名肯定是听过得,但是真正使用的人可能并不多,因为Git的产生和使用和Unix的理念是一样的,它是为技术人员所发明的,**假设使用者比设计者更清楚自己要干什么**. Git提供了管理开源代码的规范,而github是一个远程的仓库,你可以将你所有的开源代码上传到Github,而git的优越之处在于,你可以使用简洁的规则上传,记录修改,下载,分支开发,而且管理的结构性很优秀.

Git是一种分布式的代码管理软件,或者更好的说法是规范. Git的使用很简单,Linux/Unix下`man git`就可以得到所有的信息, 但是一般困扰大家的应该是对Git的理解不清晰,理解清楚了自然使用的问题也会解决. 最后附上了一个我自己写的Git初始化[shell script](https://github.com/chris-void/hellogit) 建议还是手动执行一遍对git理解会比较深刻.

## 关于Pro Git

[Pro Git下载地址](http://ishare.iask.sina.com.cn/f/23292123.html)

Git流行的原因:

**从集中管理式迁移到分布管理式**

ADV:

+ 保证数据安全
+ 方便交流
+ 方便层次模型的工作流


### Git特点

+ 利用快照: 直接比较指纹信息,未变动则link
+ 所有操作仅本地即可进行(除pull push)

### Git状态

+ commited 已提交到本地数据库
+ modifird 已修改
+ staged   已暂存

![状态示意图](http://git.oschina.net/progit/figures/18333fig0106-tn.png)

+ **已提交**: 表示该文件已经被安全地保存在本地数据库中了
+ **已修改**: 表示修改了某个文件,但还没有提交保存
+ **已暂存**: 表示把已修改的文件放在下次提交时要保存的清单中。

Git管理项目时,文件流转的三个工作区域:Git的**本地数据目录**,**工作目录**以及**暂存区域**。

每个项目都有一个git目录,它是Git用来保存元数据和对象数据库的地方。该目录非常重要,每次克隆镜像仓库的时候,实际拷贝的就是这个目录里面的数据。

从项目中取出某个版本的所有文件和目录,用以开始后续工作的叫做工作目录。这些文件实际上都是从git 目录中的压缩对象数据库中提取出来的,接下来就可以在工作目录中对这些文件进行编辑。

所谓的暂存区域只不过是个简单的文件,一般都放在git目录中。有时候人们会把这个文件叫做索引文件,不过标准说法还是叫暂存区域。

基本的Git工作流程如下所示: 

* 在工作目录中修改某些文件。
* 对这些修改了的文件作快照,并保存到暂存区域。
* 提交更新,将保存在暂存区域的文件快照转储到git 目录中。

所以,我们可以从文件所处的位置来判断状态:如果是git 目录中保存着的特定版本文件,就属于已提交状态;如果作了修改并已放入暂存区域,就属于已暂存状态;如果自上次取出后,作了修改但还没有放到暂存区域,就是已修改状态。


```
git status

.gitnore

git diff

git log
```


### git branch

+ trunk 开发
+ dev 版本
+ debug

### 分布式问题

```
git pull

git merge

git push
```




[git-https-to-ssh](https://help.github.com/articles/changing-a-remote-s-url/#switching-remote-urls-from-https-to-ssh)


