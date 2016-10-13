# tss代码规范

## 框架与技术
TSS现阶段是一个单页应用.前端静态资源服务器暂定为Apache,后端大部分情况下只提供数据交换接口.

TSS使用Spring boot框架,文档地址为http://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/.

前端使用react,使用ant-design组件库及其设计风格,使用dva框架.

数据层使用spring-data-jpa与hibernate,文档地址为http://docs.spring.io/spring-data/jpa/docs/current/reference/html/

数据库使用mysql

文档大部分使用gitbook,少数内部文档视情况而定.

集成服务器 待定.

## 规范
1. `java`中类名大写字母开头,包名小写字母开头
2. 不读取外部文件,配置文件的信息采用spring boot的配置注入方式.
3. 所有依赖的包均在pom中声明,不依赖本地下载的jar文件.
3. 区分开发环境和生产环境,使用不同的配置文件和数据库.
5. 层与层之间只依赖接口,依赖全部采用`注入`方式.
6. 各层的service均要经过测试,写操作要回滚.
