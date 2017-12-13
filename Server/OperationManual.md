涵盖常用的操作命令，默认系统Centos7+

# 查看系统信息

## 系统
- uname -a  查看内核/操作系统/cpu信息    
Linux localhost.localdomain 3.10.0-514.el7.x86_64 #1 SMP Tue Nov 22 16:42:41 UTC 2016 x86_64 x86_64 x86_64 GNU/Linux
- cat /proc/cpuinfo 查看cpu信息
- cat /etc/redhat-release 查看操作系统信息
- hostname 查看计算机名
- lspci -tv 列出所有PIC设备
- lsusb -tv 列出所有USB设备
- lsmod 列出加载的内核模块
- env 查看环境变量

## 资源
- free -m 查看内存及交换区使用量
- df -h     查看各分区使用情况
- du -sh <目录名> 查看指定目录的大小
- grep MemTotal /proc/meminfo 查看内存总量
- grep MemFree /proc/meminfo 查看空闲内存量
- uptime    查看系统运行时间、用户数、负载
- cat /proc/loadavg 查看系统负载

## 磁盘和分区
- mount | column -t 查看挂载的分区状态
- fdisk -l 查看所有分区
- swapon -s 查看所有交换分区
- hdparm -i /dev/hda 查看磁盘参数（IDE设备）
- dmesg | grep IDE 启动时IDE设备检测状况

## 网络
- ifconfig 所有网络接口属性
- iptables -L 防火墙设置
- route -n 路由表
- netstat -lntp 查看所有监听端口
- netstat -antp 所有建立的连接
- netstat -s 网络统计信息

## 进程
- ps -ef  查看所有进程
- top 实时显示进程状态
-

## 用户
- w 查看活动用户
- id <用户名> 查看指定的用户信息
- last 查看用户登录日志
- cut -d: -f1 /etc/passwd 查看系统所有用户
- cut -d: -f1 /etc/group 查看系统所有组
- crontab -l 当前用户计划任务

## 服务
- chkconfig --list 列出所有系统服务
- chkconfig --list | grep on  启动的系统服务

## 程序
- rpm -qa 所有安装的软件包
