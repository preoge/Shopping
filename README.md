# Shopping
## 简单介绍
本项目使用Spring+SpringMVC实现了一个简易的网上商城系统，使用maven构建为war包进行部署，使用docker运行。
部分代码为chatgpt协助编写，框架源码来源于开源平台
前端来自网上开源项目并做部分修改
部署时，数据库来自docker远程镜像，终端输入 docker ps即可查看远程镜像投影端口，再使用图形化数据库工具查看和修改



# 编译war包
mvn clean package -DskipTests

# 构建镜像
docker-compose build

# 启动mysql和shopping
docker-compose up -d

在http://[server-ip]:8080/Shopping访问主页。

## 默认用户
- user: user1
- password: 123

- user: admin
- password: admin

## 主要功能
1. 普通用户
    - 登录、注册功能
    - 浏览商品功能
    - 搜索商品功能
    - 查看商品详情
    - 添加购物车
    - 购买功能（在商品详情页单独购买或在购物车批量购买）
    -
2. 管理员
    - 拥有普通用户所有功能
    - 查看、删除所有用户功能
    - 查看、删除所有商品功能
    - 添加新的商品功能
    - 处理订单功能
