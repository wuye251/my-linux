# 概念

`nohup`一般用作后台执行脚本，英文全称`no hang up`(不挂起), 意思是系统后台不挂断的运行命令，退出中断不会影响程序的运行.如：`nohup ./test.sh &`

# 格式

nohup执行的格式如下：

`nohup Command [Arg ...] [&]`

- Command：要执行的命令 如 `./test.sh`要执行这个脚本
- Arg: 相关参数，如将输出信息 输出到指定文件中 ` > info.log`
- **&：让命令在后台执行，终端退出后命令继续执行**

# 样例

一般实际场景执行是：`nohup ./test.sh > test.log 2>&1 &`(后台执行./test.sh命令并将输出信息指定到test.log中)

**2>&1** 解释：

将标准错误 2 重定向到标准输出 &1 ，标准输出 &1 再被重定向输入到 runoob.log 文件中。

- 0 – stdin (standard input，标准输入)
- 1 – stdout (standard output，标准输出)
- 2 – stderr (standard error，标准错误输出)