- [1.TCP建立连接](#1.TCP建立连接)
  - [1.1 TCP套接字编程](#1.1 TCP套接字编程)
  - [1.2 半连接队列和全连接队列](#1.2 半连接队列和全连接队列)



# 计算机网络问题

## 1.TCP建立连接

### 1.1 TCP套接字编程

在Tcp建立连接的过程中，首先服务端会提前对到来的请求创建一个套接字，也可以叫做欢迎套接字。服务端调用bind()绑定自己的ip和端口号。紧接着，服务端调用accept()方法，这个方法本意是从连接队列里面取出连接，在服务器刚启动时，此时连接队列里面是空的，因此此时服务端会陷入阻塞，等待

