# Java基础 
# 内存模型
## 主内存和工作内存
java内存模型规定所有变量都储存在主内存中，每条线程都有自己的工作内存，工作内存保存了该线程使用到的变量的主内存副本的拷贝，线程对变量的操作都在工作内存中进行。<br>
```volatile型变量：此变量对所有线程可见，一个线程修改了该变量的值，其他线程可以立即得知，而普通的变量的值在线程之间的传递需要通过主内存。但注意volatile并不能保证操作的原子性。（指令重排：两句并行没有依赖关系的语句执行的时候，JVM会进行指令重排，即更换程序中两个语句的执行顺序，单线程中并不影响输出结果，但是在多线程中就可能出现问题。```
# 线程管理
* 线程的创建  
继承Thread类并且覆盖run方法  
实现runnable接口使用带参数的thread构造器创建thread对象，在这个类里面重写run方法

