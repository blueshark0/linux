# 在Linux环境安装python3
1，安装相关依赖库(工具包)：
```bash
　　yum install gcc patch libffi-devel python-devel  zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel -y
```

 

2，下载python3的源代码(在linux终端下输入命令)

　　#  python 源码下载地址：https://www.python.org/ftp/python/

　　cd opt/

　　wget https://www.python.org/ftp/python/3.4.7/Python-3.4.7.tar.xz

 

3，解压缩源代码：

　　tar -xf Python-3.7.0.tgz

 

4，进入python3.7.0 目录：

　　cd python-3.7.0

 

5，生成编译脚本(指定安装目录)：

　　./configure --prefix=/opt/python37
 
6，编译：

　　make
 
7，编译成功后，编译安装。

　　make install
  
![图片](https://images2018.cnblogs.com/blog/1353608/201808/1353608-20180810152138279-1873648531.png)

 
 

8，切换到已经安装好了的python3.7目录

　　cd /opt/python37/

 

9，查看python3.7的可执行脚本文件

　　[root@localhost python37]# ls bin/

 

10，执行python3.7解释器

　　1，绝对路径执行方式一：

　　/opt/python37/bin/python3.7

　　2，相对路径执行：

　　在 bin目录下：./python3.7

　　3，添加环境变量：

　　　　1，添加软连接（用法）：

　　　　　　ln -s 源文件路径 目标文件路径

　　　　2，添加变化软连接：

　　　　　　ln -s /opt/python37/bin/python3.7 /usr/local/bin/python3

　　4，添加pip3软连接：

　　　　ln -s /opt/pyhon37/bin/pip3 /usr/local/bin/pip3

　　5，查看pip3版本

　　　　pip3 -V

 
安装django:
　　1，安装django方式1：

　　　　pip3 install django == 2.0

　　　　pip3 install django == 1.11

　　　　方式2：

　　　　　  python3 -m pip install -i https://pypi.tuna.tsinghua.edu.cn/simple django==1.11

　　2，卸载django

　　　　pip3 uninstall django

　　3，更新pip工具：

　　　　　pip3 install --upgrade pip

　　4，安装好django1.11后，配置软连接(环境变量)

　　5，启动django
