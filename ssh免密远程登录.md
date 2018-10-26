环境：debian9.4

参考：[ssh免密登录expect](https://blog.csdn.net/heqiyu34/article/details/53842126)  
[](https://blog.csdn.net/tantexian/article/details/45887857?utm_source=blogkpcl7)

网上介绍的是关于ssh使用公钥匹配登录，而这里使用的是通过安装软件包expect来实现的。

$ sudo apt-get install 

#!/usr/bin/expect
spawn ssh root@192.168.22.194
expect "*password:"
send "123\r"
expect "*#"
interact
