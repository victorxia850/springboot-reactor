# Spring Boot Reactive 系统性自学课程

从零基础到精通：掌握 Spring Reactive 响应式编程、WebFlux 实战、R2DBC 响应式数据库与 Spring Security 响应式安全。

📚 课程概述

本课程是一套完整的 Spring Reactive 生态系统学习路径，涵盖从基础 Stream 流式处理到高级响应式安全开发的全流程。通过 5 个阶段、13 个小项目，你将掌握：

✅ **Stream API**：Lambda 表达式、函数式接口、Stream 流式操作
✅ **Reactor 核心**：Flux、Mono、响应式信号、弹珠图、背压机制
✅ **WebFlux 实战**：响应式 Web 框架、路由、过滤器、异常处理、SSE
✅ **R2DBC 响应式数据库**：响应式数据库操作、子查询、关联查询
✅ **Spring Security 响应式安全**：认证、授权、权限管理、响应式用户详情服务

🗂️ 课程目录

**第一阶段：Stream API基础（Chapter 01）**

| 课程 | 主题 | 核心内容 |
|------|------|----------|
| Chapter 01-01 | Lambda 表达式 | 函数式接口、Lambda 语法糖、BiConsumer、Function、Predicate |
| Chapter 01-02 | Stream 流式操作 | Stream API、函数式编程、集合操作、函数引用 |
| Chapter 01-03 | Flow响应式基础 | Java Flow API、发布订阅模型、SubmissionPublisher |

**第二阶段：Reactor 响应式编程（Chapter 02）**

| 课程 | 主题 | 核心内容 |
|------|------|----------|
| Chapter 02-01 | Flux 核心 | Flux 创建、订阅、流操作符、弹珠图 |
| Chapter 02-02 | 信号与事件感知 | doOnXxx 钩子函数、SignalType、BaseSubscriber |
| Chapter 02-03 | 背压与调度 | 背压机制、request(n)、Scheduler、subscribeOn |

**第三阶段：Spring WebFlux 实战（Chapter 03）**

| 课程 | 主题 | 核心内容 |
|------|------|----------|
| Chapter 03-01 | WebFlux 快速入门 | WebFlux 框架、路由函数、响应式 Controller |
| Chapter 03-02 | WebFlux 配置 | 自定义配置、静态资源、CORS跨域 |
| Chapter 03-03 | 请求与响应 | @RequestParam、@RequestBody、ServerHttpRequest/Response |
| Chapter 03-04 | 过滤器与异常处理 | WebFilter、GlobalExceptionHandler、SSE 服务端推送 |
| Chapter 03-05 | WebFlux 测试 | 响应式单元测试、WebFluxTest |

**第四阶段：R2DBC 响应式数据库（Chapter 04）**

| 课程 | 主题 | 核心内容 |
|------|------|----------|
| Chapter 04-01 | R2DBC 基础 | R2DBC 配置、DatabaseClient、响应式数据库操作 |
| Chapter 04-02 | 实体映射 | @Table、@Id、@Transient、实体类设计 |
| Chapter 04-03 | Repository 响应式查询 | BookRepostory、AuthorRepositories、自定义查询方法 |
| Chapter 04-04 | 关联查询 | 一对多、多对多、子查询、join 查询 |
| Chapter 04-05 | 类型转换器 | Converter、响应式数据类型转换 |

**第五阶段：Spring Security 响应式安全（Chapter 05）**

| 课程 | 主题 | 核心内容 |
|------|------|----------|
| Chapter 05-01 | Security 基础配置 | SecurityWebFilterChain、认证规则、表单登录 |
| Chapter 05-02 | 响应式认证 | ReactiveUserDetailsService、UserDetailsRepositoryReactiveAuthenticationManager |
| Chapter 05-03 | 权限管理 | 角色、权限、@EnableReactiveMethodSecurity、方法级权限控制 |
| Chapter 05-04 | R2DBC 集成 | 结合 R2DBC 实现数据库用户认证、密码加密 |

🚀 快速开始

**1. 环境准备**

```bash
# 安装 Java 17+（如未安装）
brew install openjdk@17

# 验证 Java 版本
java -version

# 安装 Maven（如未安装）
brew install maven
```

**2. 项目结构**

```
springboot-reactor/
├── chapter01-stream/ # Stream API 基础
│   └── src/main/java/com/victorxia/
│       ├── lambda/            # Lambda 表达式
│       └── flow/              # Flow 响应式
├── chapter02-reactor/          # Reactor 响应式编程
│   └── src/main/java/com/victorxia/reactor/
├── chapter03-webflux/          # Spring WebFlux 实战
│   └── src/main/java/com/victorxia/webflux/
│ ├── controller/        # 控制器
│       ├── config/            # 配置类
│       ├── filter/            # 过滤器
│       └── exception/         # 异常处理
├── chapter04-r2dbc/           # R2DBC 响应式数据库
│   └── src/main/java/com/victorxia/r2dbc/
│       ├── entity/ # 实体类
│       ├── repositories/      # 响应式 Repository
│       └── config/            # 配置类
├── chapter05-security/        # Spring Security 响应式安全
│   └── src/main/java/com/victorxia/security/
│       ├── entity/           # 权限实体
│       ├── config/           # 安全配置
│       └── component/        # 安全组件
└── pom.xml                   # 父级 Maven 配置
```

**3. 运行课程示例**

```bash
# 编译整个项目
mvn clean install

# 运行第一章 Stream 示例
cd chapter01-stream
mvn spring-boot:run

# 运行第二章 Reactor 示例
cd chapter02-reactor
mvn spring-boot:run

# 运行第三章 WebFlux 示例
cd chapter03-webflux
mvn spring-boot:run

# 运行第四章 R2DBC 示例
cd chapter04-r2dbc
mvn spring-boot:run

# 运行第五章 Security 示例
cd chapter05-security
mvn spring-boot:run
```

**4. 运行测试**

```bash
# 运行所有测试
mvn test

# 运行特定模块测试
cd chapter04-r2dbc
mvn test
```

🛠️ 核心技术栈

| 技术 | 用途 | 版本要求 |
|------|------|----------|
| Spring Boot | 应用框架 | 3.1+ |
| Spring WebFlux | 响应式 Web 框架 | 3.1+ |
| Spring Data R2DBC | 响应式数据库 | 3.1+ |
| Spring Security | 响应式安全 | 6.x |
| Project Reactor | 响应式库 | 3.x |
| Java | 开发语言 | 17+ |
| Maven | 构建工具 | 3.6+ |

📖 学习路径建议

**初学者路径（预计 6-8 周）**

- 第 1 周：完成 Chapter 01，掌握 Lambda 和 Stream 基础
- 第 2 周：完成 Chapter 02，深入理解 Flux/Mono 和响应式信号
- 第 3-4 周：完成 Chapter 03，构建第一个 WebFlux 应用
- 第 5-6 周：完成 Chapter 04，掌握 R2DBC 响应式数据库操作
- 第 7-8 周：完成 Chapter 05，实现完整的响应式安全系统

**进阶路径（预计 3-4 周）**

- 跳过基础概念，直接从 Chapter 03 开始
- 重点学习 R2DBC（Chapter 04）和 Security（Chapter 05）
- 深入理解响应式编程的背压和调度机制

💡 学习建议

✅ **最佳实践**

- 动手实践：每节课都有代码示例，务必亲自运行和修改
- 循序渐进：按照课程顺序学习，前期基础决定后期上限
- 记录笔记：建议为每个模块编写学习笔记和总结
- 调试优先：遇到问题先使用日志或调试工具理解执行流程
- 查阅文档：培养查阅官方文档的习惯，这是最重要的学习能力

⚠️ **常见陷阱**

- 不要跳过 Stream/Lambda 基础直接进入响应式编程
- 不要忽视背压机制的理解，这是响应式编程的核心
- 不要在未理解响应式流的情况下直接使用 WebFlux
- 不要忘记响应式编程是非阻塞的，思维模式需要转变
- 不要忽略错误处理，响应式流的异常处理方式不同于传统方式

🔗 **参考资源**

- 📖 [Spring Boot 官方文档](https://spring.io/projects/spring-boot)
- 📖 [Spring WebFlux 文档](https://docs.spring.io/spring-framework/reference/web/webflux.html)
- 📖 [Spring Data R2DBC 文档](https://spring.io/projects/spring-data-r2dbc)
- 📖 [Project Reactor 文档](https://projectreactor.io/docs)
- 📖 [Spring Security 官方文档](https://spring.io/projects/spring-security)
- 📖 [Reactive Streams 规范](https://www.reactive-streams.org/)

📄 **许可证**

本项目为个人学习与实践项目，仅用于学习与交流。如涉及转载，请注明出处。

祝你学习愉快！🎉