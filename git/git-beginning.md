# Git 入门笔记

Git 学习入门笔记

## 1. 起步

### 1.1 版本控制

- 本地版本控制系统，如RCS
- 集中化的版本控制系统，如CVS、SVN
- 分布式版本控制系统，如Git

### 1.2 Git 基础

#### 数据的三种状态：

- 已提交 committed 数据已经保存在本地数据库中
- 已修改 modified 文件已修改，但还没保存到数据库中
- 已暂存 staged 对已修改的文件做了标记，包含在下次提交的快照中

#### 三个工作区域：

- 工作目录 Working Directory
- 暂存区域 Staging Area
- Git仓库 Repository

![image](https://git-scm.com/book/en/v2/images/areas.png)

#### Git 工作流程

1. 修改文件，在工作目录中修改文件
1. 暂存文件，把文件的快照放入暂存区
1. 提交更新，把暂存区的文件快照存储到Git仓库目录

### 1.3 安装Git

#### 在Linux上安装

`$ sudo yum install git`

`$ sudo apt-get install git`

#### 在Mac上安装

- 安装Xcode Command Line Tools
- OSX Git 安装程序 [http://git-scm.com/download/mac](http://git-scm.com/download/mac)
- Github for Mac [http://mac.github.com/](http://mac.github.com/)

#### 在Windows上安装

- Git for Windows [http://git-scm.com/download/win](http://git-scm.com/download/win)
- Github for Windows [http://windows.github.com/](http://windows.github.com/)

### 1.4 Git 配置

#### 配置文件

1. `/etc/gitconfig` ：所有用户和仓库的通用配置
1. `~/.gitconfig` ：当前用户的配置，使用 --global 读写。
1. `.git/config` ：当前仓库配置

#### 用户信息

设置用户名称：

`$ git config --global user.name "your name"`

设置用户邮箱：

`$ git config --global user.email "name@example.com"`

如果只对当前仓库设置，不需要 `--global` 参数

#### 默认文本编辑器

设置文本编辑器

`$ git config --global core.editor emacs`

#### 检查配置信息

列出所有配置

`$ git config --list`

查看某一项配置

 `$ git config <key>`

### 1.5 获取帮助

- `$ git help <verb>`
- `$ git <verb> --help`
- `$ man git-<verb>`

## 2. Git 基础

### 2.1 获取 Git 仓库

#### 在现有目录中初始化仓库

`$ git init`

#### 克隆现有的仓库

`$ git clone <url> [<directory>]`
