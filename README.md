# AutoProcessinjection
自动进程注入

## 用途
对上线的机器自动进程注入进行维权

## 添加权限判断功能
原版代码统一注入到explorer进程，但在做权限维持的过程中发现，windows刚开机时启动的进程大部分是SYSTEM权限并没有explorer进程，为了第一时间就进程注入，于是稍微修改了代码添加了权限判断功能；如果上线机器为SYSTEM权限，则注入到lsass进程。如果是administrator和普通用户权限则注入到explorer进程，可自行修改代码注入到别的进程也行。

## 参考
```
https://github.com/AA8j/SecTools/blob/f2093f60e82d3ac17cbdb37c1cacbd49c66d8a03/CS/AutoProcessMigration/AutoProcessMigration.cna#L4
```
