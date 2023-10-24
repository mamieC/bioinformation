



# [生信小组7天班(生信星球)](https://www.umu.cn/course/?groupId=6553356&sKey=95e434bee92b2fed131129e31bf84434#/)

以转录组学为例，上游分析基于linux，包括质控、过滤、比对、定量，下游分析基于R语言，包括差异分析、富集分析以及可视化

### d1-2

***github使用***

提交到暂存区：

```shell
git commit -am "提示词"
```

上传：

```shell
git push origin main
```

--------

***搜索***

搜狗微信/搜狗知乎 https://weixin.sogou.com/

***markdown语法***

> （1）级别标题 
>
> 一个井号加空格 就是一级标题，两个井号加空格 就是二级标题，以此类推
>
> （2）代码块
>
> 两组三个反引号中间写代码，回车。如下：
>
> \```
>
> a = 1
>
> \```
>
> “```”是数字键1前面那个键，切换成英文格式打出来就是
>
> （3）引用
>
> 大于号加空格 后面写内容即可

***linux***

下面是你的linux账号和密码：
账号是：bio07
密码是：28157ba8
ip地址是：42.192.49.166

登陆方式：终端中输入 **ssh 用户名@ip地址**

或者用远程资源管理器登陆 bio07@42.192.49.166 

------------

目录：就是我们平时说的文件夹
路径：就是目录的层级位置

常用语法：

> `pwd`: print working directory 也就是显示当前路径
>
> 
>
> `mkdir` ：make directory 创建你的空目录
>
> 例： mkdir biosoft #存放生信软件
> 		mkdir project #存放生信项目
>
> 

> `ls` 显示当前目录下的列表
>
> 
>
> `cd`  接一个目录名，表示进入该目录
>
> `cd - `返回刚才的目录(而不是返回上一级目录)，cd .. 是返回上一级
>
> 主目录（家目录）：直接`cd` ，效果与**cd ~** 一致
>
> 
>
> `rm` 删除的操作对象分为三类：普通文件、空目录、有内容的目录。他们的对应的命令是略有不同的
>
> （1）删除文件--rm
>
> （2）删除空目录--rmdir
>
> （3）删除非空目录--rm -r
>
> 注意这三个命令**后面都要跟上你要删除的目录名**
>
> 
>
> `touch` : 接文件名，新建
>
> 
>
> `vi`：接文件名，新建并打开编辑	

> ​	i 进入编辑模式(英文输入法) ，左下角会显示 INSERT
>
> ​	esc 退出编辑模式
>
> ​	:x 保存并退出	
>
> 
>
> `cat`: 接文件名，查看文件内容（输出到屏幕）；内容超多的需要q退出
>
> 
>
> `head` 接文本文件名，默认输出前10行，`tail` 接文本文件名，默认输出后10行，后面加上`-n` 自定义输出几行
> 例如：`head -n 3 hello_world.txt` 【注意-n与head之间有空格，-n和3之间空格可有可无】
>
> 
>
> `cp` 复制文件
>
> 例 `cp file1 file2`  就是复制file1(例如 test.txt)，命名为file2的意思
>
> 
>
> `mv` 将文件移入文件夹，或者重命名
>
> 使用：`mv file 路径 `是移动file到某路径下
> 使用：`mv file1 file2` 是将file1重命名为file2



如果对linux想知根知底，推荐马哥Linux视频课程(bilibili)



### d3

服务器上软件的安装

安装miniconda：https://www.umu.cn/course/?groupId=6553356&sKey=95e434bee92b2fed131129e31bf84434#/sessionUrl/https%3A%2F%2Fm.umu.cn%2Fssu_3dfc56492%3FsourceTitle%3D

使用miniconda，查看已安装的软件、安装、卸载

`软件名 --help` 可以查看帮助信息



### d4

R语言基础

学习《R数据科学》

使用Rstudio：

​	1.用Rproject管理工作目录，R语言只能和**一个**文件夹进行互动

​	设置工作目录：`setwd()`  

如果你想进入名为"MyDirectory"的文件夹，你可以使用以下命令：

```R
setwd("MyDirectory")
```

如果"MyDirectory"不在你当前的工作目录下，你需要提供完整的路径。

```R
setwd("C:/Users/YourName/Documents/MyDirectory")
```

​	查看工作目录：`getwd()`

​	 "wd" 是 "working directory" 的缩写

​	工作目录是当前R环境正在读取或写入文件的文件夹或目录

​	当你尝试打开或保存一个文件时，如果你没有提供文件的完整路径，那么R会默认在当前的工作目录中查找或创建那个文件



 2. <- 赋值

    rm(list = ls())#清空所有变量

​	   快捷键`ctrl+l` 清空console

### d5 

https://www.umu.cn/course/?groupId=6553356&sKey=95e434bee92b2fed131129e31bf84434#/sessionUrl/https%3A%2F%2Fm.umu.cn%2Fssu_3dfc768cc%3FsourceTitle%3D

（1）R的赋值符号不是等号，而是<-
（2）在Console 控制台输入命令，相当于Linux的命令行 
（3）R的代码都是带括号的，括号必须是英文的。
（4）显示工作路径 getwd()
（5）元素可以是数字或者字符串character（需要加引号），向量是多个元素组成的变量（例如 c(1,2,3)），标量是一个元素组成的变量（例如 "huahua"）
（6）表格在R语言中改名叫数据框
（7）函数或者命令不会用时，用这个命令查看帮助：`?read.table`，调出对应的帮助文档，翻到example部分研究一下。
（8）数据类型（重点只有两个，剩下的不看）

> - **向量（vector）👈重要**
> - 矩阵（Matrix）
> - 数组（Array）
> - **数据框（Data frame）👈重要**
> - List

```R
x<- c(1,2,3) #常用的向量写法，意为将x定义为由元素1，2，3组成的向量。xx<- 1:10 #从1-10之间所有的整数x
x<- seq(1,10,by = 0.5) #1-10之间每隔0.5取一个数（注意是逗号不是分号）x
x<- rep(1:3,times=2) #1-3 重复2次，也可以写作x<- rep(1:3, 2) 
```

提取元素，根据元素位置：

```R
x[4] #x第4个元素
x[-4]#排除法，除了第4个元素之外剩余的元素
x[2:4]#第2到4个元素
x[-(2:4)]#除了第2-4个元素
x[c(1,5)] #第1个和第5个元素
```

提取元素，根据值：

```R
x[x==10]#等于10的元素
x[x<0]
x[x %in% c(1,2,5)]#存在于向量c（1，2，5）中的元素
```



# 单细胞转录组学习

### 第1部分RNA Seq的基础知识

![image-20231022165812771](https://my-bed.oss-cn-shanghai.aliyuncs.com/img/image-20231022165812771.png)

WGS：全基因组测序

WES：全外显子测序

练习资料：

> https://disk.pku.edu.cn:443/link/AF607A65FC8133894B9767885DEAC400
>
> or命令行
>
> wget https://www.bioinfo.info/tmp/data/test_R1.fq.gz
> wget https://www.bioinfo.info/tmp/data/test_R2.fq.gz     
>
> wget https://www.bioinfo.info/tmp/data/md5.txt

linux学习https://www.lanqiao.cn/courses/1



RNA：按绝对数量排序

rRNA，tRNA，mRNA，snRNA，snoRNA，miRNA 

查找mRNA的信息（例如定位、功能、疾病……），使用：Uniprot 网站

miRNA 的database：miRBase



### 第2部分RNA-Seq的mapping





### 第3部分RNA-Seq的定量及标准化





### 第4部分寻找差异表达基因





### 第5部分RNA-Seq的注释分析





### 第6部分RNA-Seq的可变剪切分析







### 第7部分多样本RNA-Seq分析





### 





















