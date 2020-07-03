# Markdown的使用
## 1.标题
使用一个或多个（至多6个）# ，来定义标题等级。

## 2.引用
使用>表示引用

## 3.清单列表
+ 输入1. 表示创造一个有序列表

+ 输入* ，-，+等表示创造一个无序列表

## 4.程序代码块
+ 输入```创造一个程序代码块

+ 输入：创造一行代码

## 5 .数学符号
输入$$创造数学公式

## 6.分隔符
输入***，+++，---等创造一个分割符

## 7.表格
输入|第一列|第二列|...创造一个表格

## 8.脚注
输入[^脚注]插入脚注

## 9.目录
输入[toc]插入一个目录

## 10.链接
如，输入：[]():[git](http://github.com/)

## 11.图片
输入![]()

## 12.斜体和加粗
+ 输入*斜体字*

+ 输入**加粗字**

# Linux的使用
## 1.磁盘管理命令
+ pwd：显示当前所在目录位置

+ cd 目录名：切换目录

+ ll,ls ：列出当前目录下目录及文件

## 2.文件管理命令
+ mkdir 目录名：创建目录

+ rm 删除文件：删除文件

+ rm -rf 删除目录：删除目录

+ cp 复制文件 新文件名：复制文件

+ cp -rf 复制文件夹 新文件夹名：复制文件夹

+ cat 文件路径：显示一个文件的所有内容

+ more 文件路径：空格一页一页展示，enter一行一行展示

+ head -n 数字 文件名：显示文件头部，默认10行

+ tail -n 数字 文件名：显示文件尾部，默认10行

+ grep [参数] 搜索的字符串内容 文件名1 [文件n]：文件搜索（区分大小写）

## 3.管道
+ echo "内容">文件名：将内容写到该文件中（覆盖原内容）

+ echo "内容">>文件名：将内容写到该文件中（追加内容）

+ 命令1|命令2|命令3...

## 4.系统命令
+ date ：显示当前系统时间

+ clear：清屏

+ reboot：重启linux

+ shutdown：关机

+ ps -ef：查看当前系统进程

+ kill -pid ：结束一个进程，pid是由ps -ef查出来的

## 5.压缩解压命令
+ tar 参数 要压缩或解压的文件或目录：压缩（归档），文件扩展名为tar.gz

  参数包括： z 压缩，c 创建压缩文档，v 显示压缩，解压过程中处理的文件名

  创建归档文件，如：tar -zcvf test.tar.gz 文件名

+ tar -tf 压缩文件名：查看归档文件的内容

+ tar -zxvf 压缩文件 -C 目标目录：解压文件到目标目录下，默认是当前目录

## 6.网络通信
ping 网址

## 7.网络访问
+ curl 网址

+ wget 下载资源的地址

## 8.vi和vim
vi 文件名：启动vi编辑器

命令模式：esc，进入命令模式，此时无法编辑

编辑模式：按a或i字母键，进入编辑模式，此时按：:wq 保存退出，:q!不保存退出

	dd：删除光标所在行

	yy：复制光标所在行到缓冲区

	p：粘贴缓冲区中的内容

	gg：光标回到文件第一行
			
	GG：光标回到文件最后一行

	^：光标回到当前行行首

	S：光标回到当前行行尾

	/关键字：搜索寻找的字符，一直按n可以向后寻找
## 9.安装软件命令
+ sudo apt search 关键字 寻找安装文件

+ sudo apt install

+ sudo apt remove

## 10.权限授予
su root 授予root权限 r代表可读，用4表示。 w 代表可写，用2表示。 x 代表可执行，用1表示。

# Linux启动过程（开机启动顺序）
+ 第一步－－加载BIOS

+ 第二步－－读取MBR

+ 第三步－－Boot Loader

+ 第四步－－加载内核

+ 第五步－－用户层init依据inittab文件来设定运行等级

+ 第六步－－init进程执行rc.sysinit

+ 第七步－－启动内核模块

+ 第八步－－执行不同运行级别的脚本程序

+ 第九步－－执行/etc/rc.d/rc.local

+ 第十步－－执行/bin/login程序，进入登录状态

# Linux模块
+ rfcomm

+ bluetooth

+ videodev

+ videobuf2_vmalloc

+ videobuf2_memops

+ videobuf2_core

+ media

+ memstick
# git的使用
## 1.创建本地仓库
空的：git init
## 2.配置信息
+ git config --global user.email '13633217285@163.com'

+ git config --global user.name 'favorrite'
## 3.添加到暂存区
git add 文件名
## 4.查看状态
git status
## 5.提交
git commit -m '备注'
## 6.修改
git push
## 7.恢复文件
git checkout 文件名
## 8.查看历史版本
git log （方便恢复）
## 9.恢复版本
git reset --hard 版本号
## 10.生成ssh密匙
ssh-keygen -t rsa -C "github的邮箱地址"
## 11.从暂存区修改至远程仓库
+ git remote add origin 仓库网址

+ git push -u origin master
## 12.更新文件，同步文件
git pull
