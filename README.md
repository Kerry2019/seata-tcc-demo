## 1、目录结构说明
1. eureka-server：eureka注册中心
2. account-service：用户账户服务
3. storage-service：商品库存服务
4. order-service：订单服务
5. resources/database-sql：mysql数据库表结构的初始化脚本
6. resources/seata-server：seata server服务的配置文件 file.conf、registry.conf

## 2、启动顺序
1. resources/database-sql：初始化数据库
2. eureka-server：运行注册中心
3. resources/seata-server：下载、安装、配置、启动 seata server服务
4. account-service：运行用户账户服务
5. storage-service：运行商品库存服务
6. order-service：运行订单服务
7. 测试：通过postman等工具，调用 order-server 的下订单接口