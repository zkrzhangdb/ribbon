服务消费者   负载均衡

依次启动eureka-server、compute-service、eureka-ribbon工程
访问http://localhost:1111/可以看到注册中心的状态
访问http://localhost:3333/add，调用eureka-ribbon的服务，该服务会去调用compute-service的服务，计算出10+20的值，页面显示30
关闭compute-service服务，访问http://localhost:3333/add，我们获得了下面的报错信息




验证断路器的回调
依次启动eureka-server、compute-service、eureka-ribbon工程
访问http://localhost:1111/可以看到注册中心的状态
访问http://localhost:3333/add，页面显示：30
关闭compute-service服务后再访问http://localhost:3333/add，页面显示：error
