---
title: happens-before 原则
date: 2019-7-24 19:20:31
categories:
 - JMM
tags:
 - 
---
java happens-before 原则
## 原则

1. 程序次序法则：线程中的每个动作A都happens-before于该线程中的每一个动作B，其中，在程序中，所有的动作B都能出现在A之后。
2. 监视器锁法则：对一个监视器锁的解锁 happens-before于每一个后续对同一监视器锁的加锁。
3. volatile变量法则：对volatile域的写入操作happens-before于每一个后续对同一个域的读写操作。
4. 线程启动法则：在一个线程里，对Thread.start的调用会happens-before于每个启动线程的动作。
5. 线程终结法则：线程中的任何动作都happens-before于其他线程检测到这个线程已经终结、或者从Thread.join调用中成功返回，或Thread.isAlive返回false。
6. 中断法则：一个线程调用另一个线程的interrupt happens-before于被中断的线程发现中断。
7. 终结法则：一个对象的构造函数的结束happens-before于这个对象finalizer的开始。
8. 传递性：如果A happens-before于B，且B happens-before于C，则A happens-before于C











