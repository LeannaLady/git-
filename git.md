# git提交 移除untracked及add的文件
============================
在我们实际开发提交代码时会碰到当前状态下的文件并不全是自己想要提交的内容，这个时候最基础的办法就是我们使用:

**git checkout out +文件**

**rm +文件**

来剔除我们不需要的文件。
	但如果有很多未提交的更改（Changes not staged for commit）文件及untracked files文件，用这种方式就有点费时费力惹人烦了。今天就告诉大家一个非常好用的方法。
	
1.首先添加需要提交的文件

**Git add 要提交的文件**

然后查看那剩下的会删除的文件

**git clean -fd -n**

其次执行删除新增加的无用的文件目录

**Git clean -df**

最后删除modify的文件

**Git checkout .**

这样就完美解决了！
