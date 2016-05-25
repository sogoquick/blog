###如何使用GDB 调试C项目
```
Mac 下 brew 安装 GDB

brew install gdb

```

*****然后运行 gdb 在Mac 下需要sudo 执行，不然回报扩展库无法执行错误*****

****BTW : ****

```

gcc 工程时 需要带上 -g 参数

或者 make 时加上 CFLAGS="-g -O0"

```

For Example ：

Debug Memcached

```
1、 ./configure

2、make CFLAG="-g -o0"

3、make install

4、sudo gdb memcached

5、设置中断调试点, 如： b main

###
memcached 不能以root 权限执行，所以此处需要加参数 -u sogoquick
6、r -p 11211 -u sogoquick -vvv 


```

#####参考资料
[Mecached Debug 及源码阅读](http://mamicode.com/info-detail-418163.html)

[memcached debugger gdb](http://blog.csdn.net/unix21/article/details/15501049)