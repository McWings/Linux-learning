# Bash命令
## 一、man 命令
    An interface to the on-line reference manuals.
    一个在线参考说明的接口。
###  man命令中常用按键及用途
    空格键==>向下翻页
    PG Down==>向下翻页
    PG UP==>向上翻页
    Home==>跳转到首页
    End==>调转到尾页
    /==>从上至下搜索关键词，例“/关键词”
    ?==>从下至上搜索关键词，例“?关键词”
    n==>定位到下一个搜索目标
    N==>定位到上一个搜索目标
    q==>退出
### man命令帮助信息结构及意义
    NAME==>命令的名称
    SYNOPSIS==>参数的大致使用方法
    DESCRIPTION==>详细描述
    EXAMPLES==>演示（附带简单说明）
    OVERVIEW==>概述
    DEFAULTS==>默认的功能
    OPTIONS==>具体的可用选项
    ENVIRONMENT==>环境变量
    FILES==>用到的文件
    SEE ALSO==>相关资料
    HISTORY==>维护历史与联系方式
## 二、echo命令
    Display a line of text.显示一行文本。
### 用法
    echo test==>在屏幕上打印文本
    echo $变量==>在屏幕上显示变量的值
## 三、date命令
    date 命令用于显示及设置系统的时间或日期。
### date命令中的参数
    | 参数 | 作用 |
    |:-----:|:-----:|
    |%t|跳格【TAB键】|
    |%H|小时（24小时制）|
    |%I|小时（12小时制）|
    |%M|分钟|
    |%S|秒|
    |%j|今年的第X天|
    |%Y|年|
    |%y|年（末2位）|
    |%m|月|
    |%d|日|

用法
date==>显示系统时间（星期 月 日 时:分:秒 CST 年 ）
date "+%X"==>以指定格式显示系统时间
date -s "YYYYmmdd HH:MM:SS"==>设置系统时间
## 四、halt命令
halt命令用于关闭系统，同时包括poweroff命令和reboot命令。
用法
halt -p==>关机
halt -r==>重启
halt -f==>强制关闭
## 五、wget命令
The non-interactive network downloader.无交互式网络下载器。
wget命令用于在终端中下载网络文件。
用法
wget -b==>后台下载模式
wget -P==>下载到指定目录
wget -t==>最大尝试次数
wget -c==>断点续传
wget -p==>下载页面内所有资源，包括图片、视频等
wget -r==>递归下载
## 六、ps命令
Report a snapshot of the current processes.生成一个当前进程的简要说明。
ps命令用于查看系统中的进程状态。
用法
ps -a==>显示所有进程（包括其他用户的进程）
ps -u==>用户以及其他详细信息
ps -x==>显示没有控制终端的进程
进程状态
R（运行）：进程正在运行或在运行队列中等待。
S（中断）：进程处于休眠中，当某个条件形成后或者接收到信号时，则脱离该状态。
D（不可中断）：进程不响应系统异步信号，即便用 kill 命令也不能将其中断。
Z（僵死）：进程已终止，进程描述符仍存在, 父进程调用 wait4()系统函数后释放进程。
T（停止）：进程收到停止信号后停止运行。
当执行ps aux命令后会看到如下所示进程状态：

状态名称USERPID%CPU%MEMVSZRSSTTYSTATSTARTTIMECOMMAND含义说明所属用户进程ID运算器占用率内存占用率虚拟内存用量(KB)占用的固定内存量(KB)所在终端进程状态启动时间占用CPU时间命令名称与参数示例root100400.00.0115442116tty1Ss07:220:02/usr/lib/systemd/systemd

## 七、top命令
Display Linux processes.显示Linux进程。
top命令用于动态地监视进城活动与系统负载等信息。
管理器界面说明
第 1 行：系统时间、运行时间、登录终端数、系统负载（三个数值分别为 1 分钟、5分钟、15 分钟内的平均值，数值越小意味着负载越低）。
第 2 行：进程总数、运行中的进程数、睡眠中的进程数、停止的进程数、僵死的进程数。
第 3 行：用户占用资源百分比、系统内核占用资源百分比、改变过优先级的进程资源百分比、空闲的资源百分比等。 
第 4 行：物理内存总量、内存使用量、内存空闲量、作为内核缓存的内存量。
第 5 行：虚拟内存总量、虚拟内存使用量、虚拟内存空闲量、已被提前加载的内存量。
​​
## 八、pidof命令
Find the Process ID of a running program.找到正在运行程序的进程编号。
pidof 命令用于查询某个指定服务进程的 PID 值。
## 九、kill命令
Terminate a process.中止一个进程。
kill 命令用于终止某个指定 PID 的服务进程。
## 十、killall命令
    Kil processes by name.按名称结束进程。
    killall 命令用于终止某个指定名称的服务所对应的全部进程。

> 如果有些命令在执行时不断在屏幕上输出信息，影响到后续命令的输入，可以在输入命令时，在末尾添上一个"&"符号，命令就会在系统后台执行。






















































































