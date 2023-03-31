# 系统规划
- [x] 基础业务管理平台：Razor+Vue+H5+小程序+APP；
- [x] 基础业务管理平台：Razor&vue&bootstrap&layui+mvc+ddd+ef；
- [x] 接口管理平台：业务接口&微信接口的服务化管理(跨平台&微服务化)；
- [x] gitlab&azuredevopsserver+接口文档平台+禅道+企业微信(知识库，在线课堂)；
- [x] 放弃abp,saas(组织和租户)，devops

# 计算机知识点

- [x] 内存数据结构及原理：数据结构类型，存储方式；
- [x] CPU多线程异步原理：io操作，异步操作，多线程操作；
- [x] 网络通信协议及原理：网络模型，http，tcp原理，rpc原理；
- [x] 并发事务锁机制：cap事务一致性，悲观锁乐观锁，redis锁防止并发竞争 抽奖秒杀库存；
- [x] 性能优化及分析：tps qps并发数，响应速度，数据库优化；
- [x] 设计模式及原则：23种设计模式[单例，工厂，桥接，适配，装饰，策略，订阅，职责链],以及6大设计原则[开闭只新增不修改，里氏不改变父类，接口隔离，依赖倒转，单一职责，迪米特尽量少和陌生人说话]；
- [x] 系统架构及演变：单体，分布式，微服务，devops；
- [x] 项目管理及设计：时间计划，研发环境，设计建模；

# 开源地址

 GitHub：GitHub:https://github.com/luoyesong102；

## 基础业务平台

说明：（Base.Common.Manager）开箱即用企业级业务系统【 Razor+Mvc+DDD+Ef+WebApi+H5】框架,配套用户基础权限管理后台进行使用


### 前端功能与进度

- [x] 采用原生BootStrap布局，Div展示页面(少数页面会用Iframe打开窗口)，Razor渲染视图；
- [x] 封装了主界面LayOut模板，单页面下ifame下的iframedatable模板和datatable模板；
- [x] 采用后台控制js和css样式的引入,并分类管理,引入了layui,hplusui等框架； 
- [x] 引入了各种组件，如下拉树，下拉列表，警告框，弹出层等,自定义了 MvcHtml的组件； 
- [x] 封装了核心main.js主要用于ajax和模态框的使用；
- [x] 封装了核心datatable.js操作库用户table的数据渲染操作；  
- [x] 简化了界面参数赋值的操作；
- [x] 简化了页面带条件查询的列表开发周期；
- [ ] 参数自动赋值,并不是万能；
- [ ] datatable模板，并不是万能；
- [ ] 组件还不够丰富，未来会通过Layui和Vue进行丰富；

### 后端功能与进度

- [x] 采用H5+WebApi+Mvc+DDD+EF的形式封装框架；
- [x] 使用MiniProfiler做接口性能分析；
- [x] 使用Automapper做Dto处理；
- [x] 接入EF+Dapper ORM，封装仓储层进行数据库操作；  
- [x] AutoFac接入做依赖注入；
- [x] 支持AOP切面编程；
- [x] 支持CORS跨域；
- [x] 丰富的公共组件,如Redis/RBMQ 队列等；
- [x] 支持相关配置信息内存化及开关切换；
- [x] 支持编写SQL进行统一管理及加载；
- [x] 支持多系统单点切换；
- [x] 独立的权限管理系统；




## 接口管理平台

说明：（Blog.Core&Vue Project）开箱即用的企业级前后端分离【 .NET Core3.1 Api + Vue 2.x + RBAC】权限框架，用来管理接口权限。 

### 功能与进度

#### 商业授权付费版下🎁🎁🎁

- [x] 包含下边框架模块中的所有功能；
- [x] 全部表结构主键底层架构改成`string`类型（默认雪花，支持guid），更方便迁移；
- [x] 完善部门数据权限，可以基于策略配置查看数据范围；
- [x] 优化权限处理器，解决多实例分布式下，权限不同步问题（必须配置Redis）；
- [x] 增加在线用户查看功能，并实现强制用户下线功能（必须配置Redis）；
- [x] 增加用户黑名单功能（必须配置Redis）；
- [x] 增加岗位功能（单独建表），配合部门使用；
- [ ] 后期优化站内通知功能，其实目前已经有SignalR来实现消息推送了，可以直接用；
- [ ] 前端`Blog.Admin.Pro`使用`AntDesignVue`框架（设计中，未完全实现）；
- [x] 铁粉奖励：如果参与上述功能和其他付费功能开发，可半价获取商业授权；



#### 框架模块：  
- [x] 采用`仓储+服务+接口`的形式封装框架；
- [x] 自定义项目模板 `CreateYourProject.bat` ，可以一键生成自己的项目；🎶  
- [x] 异步 async/await 开发；  
- [x] 接入国产数据库ORM组件 —— SqlSugar，封装数据库操作，支持级联操作；
- [x] 支持自由切换多种数据库，MySql/SqlServer/Sqlite/Oracle/Postgresql/达梦/人大金仓；
- [x] 实现项目启动，自动生成种子数据 ✨； 
- [x] 实现数据库主键类型配置化，什么类型都可以自定义 ✨； 
- [x] 五种日志记录，审计/异常/请求响应/服务操作/Sql记录等,并自动持久化到数据库表🎶； 
- [x] 支持项目事务处理（若要分布式，用cap即可）✨；
- [x] 设计4种 AOP 切面编程，功能涵盖：日志、缓存、审计、事务 ✨；
- [x] Log4net 多种日志自动生成到数据库中，目前支持MySql/SqlServer/Sqlite/Oracle/Postgresql🎉；
- [x] 设计并支持按钮级别的RBAC权限控制，同时支持一键同步接口和菜单 🎶；
- [x] 支持 T4 代码模板，自动生成每层代码；
- [x] 或使用 DbFirst 一键创建自己项目的四层文件（支持多库）；
- [x] 封装`Blog.Core.Webapi.Template`项目模板，一键重建自己的项目 ✨；
- [x] 搭配多个前端案例供参考和借鉴：Blog.Vue、Blog.Admin、Nuxt.tbug、Blog.Mvp.Blazor ✨；
- [x] 统一集成 IdentityServer4 认证 ✨;
- [x] 统一实现多租户;  


组件模块：
- [x] 提供 Redis 做缓存处理；
- [x] 使用 Swagger 做api文档；
- [x] 使用 MiniProfiler 做接口性能分析 ✨；
- [x] 使用 Automapper 处理对象映射；  
- [x] 使用 AutoFac 做依赖注入容器，并提供批量服务注入 ✨；
- [x] 支持 CORS 跨域；
- [x] 封装 JWT 自定义策略授权；
- [x] 使用 Log4Net 日志框架，集成原生 ILogger 接口做日志记录；
- [x] 使用 SignalR 双工通讯 ✨；
- [x] 添加 IpRateLimiting 做 API 限流处理;
- [x] 使用 Quartz.net 做任务调度（目前单机多任务，集群调度暂不支持）;
- [x] 支持 数据库`读写分离`和多库操作 ✨;
- [x] 新增 Redis 消息队列 ✨;
- [x] 新增 RabbitMQ 消息队列 ✨;
- [x] 新增 EventBus 事件总线 ✨;
- [x] 新增 - 统一聚合支付;
- [x] 新增 - Nacos注册中心配置;
- [x] 新增 - ES 搜索配置;
- [x] 新增 - Apollo 配置;
- [x] 新增 Kafka 消息队列，并配合实现EventBus ✨;
- [x] 新增 微信公众号管理，并集成到Blog.Admin后台 ✨;
- [x] 新增 - 数据部门权限;
- [x] 新增 - Log4net集成日志数据持久化到数据库;  
- [x] 新增 - 多租户模式（单表，多表，多库三种模式）;  


微服务模块：
- [x] 可配合 Docker 实现容器化；
- [x] 可配合 Jenkins 实现CI / CD；
- [x] 可配合 Consul 实现服务发现；
- [x] 可配合 Nacos 实现服务发现；
- [x] 可配合 Ocelot 实现网关处理；
- [x] 可配合 Nginx  实现负载均衡；
- [x] 可配合 Ids4   实现认证中心；
