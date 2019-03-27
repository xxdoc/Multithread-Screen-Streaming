# Multithread-Screen-Streaming
VB6 多线程屏幕串流

第一次尝试用VB6来弄多线程的程序... 之前曾经写过用屏幕扫描算法来传输屏幕，但是在VB6默认的情况下是单线程运行的，如果不断地扫描则会阻塞线程；如果用计时器来隔一段时间再进行扫描则看上去画面略卡。 直到在贴吧看到这个[多线程例子](http://tieba.baidu.com/p/3616346086)，决定拿来试一下。开发的时候崩了很多次（VB6真的对线程不怎么友好QWQ） 不过总算是弄完了。 其实效果一般般，在本机觉得还行，放在局域网就开始崩了

亮点：
- 多线程
- 纯API Socket （因为线程里面不能操作Winsock控件... 只好自己用APi写）
- Socket数据流处理，自己写了个缓冲区用来处理Socket的分包
- 屏幕扫描算法
