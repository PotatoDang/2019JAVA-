# JAVA学习知识点
相关基础知识，查漏补缺
--------
## [集合类](/集合类.md)
****************
集合顶层接口为单列集合Collection和双列集合Map
Collection的实现有
+ List 包含重复元素
  + ArrsyList 线程不安全
  + LinkedList 线程不安全
  + vector 线程安全
+ Set不包含重复元素
  + HashSet 线程不安全
  + LinkedHashSet 线程不安全，但保证插入顺序
  + TreeSet 基于红黑树，线程不安全
  Map的实现有
+ HashMap 线程不安全，初始容量为16，扩容为2倍，负载因子为0.75
  + JDK1.7 基于数组+链表，添加元素为头插法，put后进行扩容时形成环链导致get陷入循环
  + JDK1.8 基于数组+链表+红黑树，当链表长度达到8时，检测容量是否到64，若未到64则扩容，若大于64则转为红黑树，且添加元素为尾插法
+ TreeMap 基于红黑树，线程不安全
+ Hashtable 基于数据加链表结构，线程安全，头插法
## [多线程](/多线程.md)
****************
+ 线程与进程
+ 死锁问题
+ 线程通讯与进程通讯
  + 线程通讯依靠共享内存或静态变量，其中有wait和notify、synchronized、reentrantLock
  + 进程通讯则通过IPC，其中有管道、命名管道、消息、消息队列、信号量、Socket、共享内存
## [操作系统](/操作系统.md)
****************
:smirk:
## [Spring](/Spring.md)
****************
**IOC**

控制反转，将对象的创建权交给Spring容器，并由SPring容器进行装配，管理生命周期。
**AOP**

面向切面编程，将分散在各个业务逻辑代码中的同类代码，通过横向切割的方式抽取到一个独立模块中，是OOP的功能扩展。
## [JVM虚拟机](/虚拟机.md)
****************
 虚拟机的作用：
 + 类加载
 + 内存分配
 + 垃圾回收
   + 标记整理
   + 标记清除
   + 复制算法
   + 分代收集
 + 垃圾回收器
   + 新生代
     + Serial
     + ParNew
     + Parallel Scanvege
   + 老年代
     + Serial Old
     + Parallel Old
     + CMS
   + 不区分
     + G1 JDK1.9为默认垃圾回收器，按照region为单位进行回收，整体时标记整理，局部为复制
     + ZGC 按照page为单位进行回收，GC时进行压缩，停顿时间STW不会随着堆增大而增大，最大支持4T堆内存
## [算法](/算法.md) 
****************
**排序**
+ 冒泡排序
+ 选择排序
+ 插入排序
+ 希尔排序
+ 归并排序
+ 快速排序
+ 堆排序
+ 桶排序
+ 基数排序
+ 计数排序

**查询**
+ 二分查找

**动态规划**
迪杰斯塔拉算法
弗洛伊德算法
背包问题

**贪心算法**
## [数据库知识](/数据库.md) 
****************
关系型数据库
+ mysql：基于多表
+ oracle：多用户

非关系型数据库
+ redis：可以持久化到内存，可以存放五种类型数据
+ memcache：不可以持久化到内存，断电即消失，只可以存放字符串类型数据
+ MonoDB：
## [计算机网络](/计算机网络.md)
****************
+ 基础知识
+ 网络模型
+ 网络协议

## [IO模型](/IO模型.md)
-----
+ 操作系统五种IO模型
+ Java的三种IO
+ Netty的学习


