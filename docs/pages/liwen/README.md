### macOS下载的文件执行出现operation not permitted问题

> mac在默认情况下，运行从普通internet站点上下载的文件时都要先进行安全性提示

使用命令ls -l@会发现下载后的文件多出了后缀名com.apple.quarantine   
我们需要把这个后缀名给去掉，才不会出现即使全部授权，也不能允许运行的情况。

命令如下 
```xattr -rd com.apple.quarantine [dirname] ```
其中[dirname]就是文件夹名称，即你下载的文件夹或者解压后的文件夹即可。
