# 计算机概念 #

----------


CPU：相当于脑袋，所有活动都通过脑袋来进行判断和控制

内存：放置数据的区块。暂时存放互动数据，给CPU提供来判断的信息

硬盘：放置回忆的记忆区块。与内存不同，**内存提供目前要处理的信息**，但一些没有立刻处理的事情，存入硬盘，以便未来再次使用

主板：相当于神经系统。将所有元件连接起来


----------

![](https://raw.githubusercontent.com/PoorMonk/MarkDownPhotos/master/1.png)

在使用man page查看某些数据时，对比以上表格就知道该指令/文件所代码的基本意义了。

例如：输入命令man null，会出现的第一行是：“NULL （4）”，对比表格发现，null这玩意竟然是一个“设备文件”！

----------
## 文件的类型与权限 ##
root@poormonk-virtual-machine:~# ls -al

总用量 32

-rw-------  1 root root  137 1月  12 11:08 .bash_history

-rw-r--r--  1 root root 3106 10月 23  2015 .bashrc

drwx------  2 root root 4096 8月   1 19:27 .cache

drwxr-xr-x  3 root root 4096 12月  7 17:52 .config

drwxr-xr-x  3 root root 4096 12月  7 17:50 .local

-rw-r--r--  1 root root  148 8月  17  2015 .profile

第一个字符代表这个文件是“目录、文件或链接文件等等”：

- 当为[d]则是目录，例如上面“.config”的那一行
- 当为[-]则是文件，例如上面“.bashrc”的那一行
- 当为[l]则表示为链接文件
- 若是[b]则表示为设备文件里面的可供储存的周边设备（可随机存取设备）
- 若是[c]则表示设备文件里面的序列埠（bu)设备，例如键盘、鼠标（一次性读取设备）

接下来的字符中，以三个一组表示读写权限，没有权限则用[-]表示。第一组为“文件拥有者可具备的权限”；第二组为“加入此群组之账号的权限”；第三组为“非本人且没有加入本群组之其他账号的权限”。

权限在文件和目录之间的区别：
![](https://raw.githubusercontent.com/PoorMonk/MarkDownPhotos/master/2.png)