# jasypt-spring-boot-jasypt-spring-boot-parent-1.18 目的 修改加解密用得盐的key

jasypt-spring-boot修改加解密用得盐的key

使用得jasypt-spring-boot得版本是1.18

因为我们项目没有用springboot 2.0

拉取得是tag里面得一个分支。



项目加解密的key 盐值

用到的key 是 

jasypt.encryptor.password = yourkey

这个boot里面properties的属性值，要配置到apollo的glabal common里面（或者每个项目组的各个项目里面都要单独配置1下）

很多人可以看到 这样就对保密性不太好 ，大家搜一下百度都知道 是盐,算法找下就可以反过来解密，


本文的目的就是给jasypt.encryptor.password 换个名字 比如看着不像是记录密钥的

举个例子

com.xxcompany.framework.info=xxcompany

xxcompany 其实就是盐 但是这样即使看着也隐蔽性很高

比原来工程改动的地方 可以搜索XXcompany 关键字 在idea里面搜*.* 范围 只有两处
其他地方对pom改了一些 方便大家打包到自己公司私服里面

大家可以看看


--------------------- 
作者：琅琊山二当家 
来源：CSDN 
原文：https://blog.csdn.net/AlbertFly/article/details/88944604 

详细说明参考上面csdn链接
