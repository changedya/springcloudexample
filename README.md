# springcloudexample
spring cloud 学习例子<br>

服务发现（Eureka、consul）<br>
&emsp;&emsp;eureka-server(服务注册中心) http://localhost:1001/ <br>
&emsp;&emsp;eureka-client(服务提供方)http://localhost:2001/demo <br>
&emsp;&emsp;eureka-consumer(服务消费者-手动负载均衡)http://localhost:2101/consumer <br>
&emsp;&emsp;eureka-consumer-ribbon(服务消费者-自动负载均衡)http://localhost:2102/ribbon <br>
&emsp;&emsp;Note:先启动注册中心然后启动服务提供者<br>
&emsp;&emsp;Eureka简介:http://www.cnblogs.com/wangdaijun/p/6851027.html<br>
&emsp;&emsp;Eureka简介:http://www.roncoo.com/article/detail/128041<br>
<p>
&emsp;&emsp;consul-client(consul服务提供方)
Spring Cloud Consul项目是针对Consul的服务治理实现<br>
&emsp;&emsp;Consul特性:服务发现,健康检查,Key/Value存储,多数据中心<br>
&emsp;&emsp;由于Consul自身提供了服务端，所以我们不需要像之前实现Eureka的时候创建服务注册中心，<br>
&emsp;&emsp;直接通过下载consul的服务端程序就可以使用。<br>
&emsp;&emsp;consul怎么在windows下安装:http://blog.csdn.net/forezp/article/details/70188595<br>
&emsp;&emsp;consul下载地址：https://www.consul.io/downloads.html<br>
&emsp;&emsp;windows pc 环境变量设置 在path下加上：E:\programfiles\consul； cmd启动运行 consul agent -dev<br>
&emsp;&emsp;consul默认地址：http://localhost:8500<br>
&emsp;&emsp;访问demo:http://localhost:3001/demo<br>
&emsp;&emsp;服务发现系统consul介绍:http://www.tuicool.com/articles/j2YVB3<br>
<p>
声明式REST客户端-Feign的使用<br>
&emsp;&emsp;Feign是一种声明式、模板化的HTTP客户端。<br>
&emsp;&emsp;在Spring Cloud中使用Feign, 我们可以做到使用HTTP请求远程服务时能与调用本地方法一样的编码体验，<br>
&emsp;&emsp;开发者完全感知不到这是远程方法，更感知不到这是个HTTP请求。<br>
&emsp;&emsp;eureka-consumer-feign(服务消费者-feign): http://localhost:2103/feign?name=hello <br>
&emsp;&emsp;feign是自带断路器的，此版本hystrix是关闭的 ，如果使用feign想用断路器的话，可以在配置文件中开启它<br>
&emsp;&emsp;配置如下：feign.hystrix.enabled=true<br>
<p>
断路器（Hystrix）<br>
智能路由（Zuul）<br>
客户端负载均衡（Ribbon）<br>

