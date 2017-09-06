ConfigX
===

不管做什么项目，都会遇到很多的配置，有简单的属性配置，有复杂的文件配置，以前这些配置都是跟代码一起打包发布的，不同的环境发布需要打不同的包，修改配置就需要重启应用，使得配置的修改代价非常大。<br>
为了解决这些问题，开发了这个配置管理系统，将所有的外化到配置管理系统中，将代码的发布与配置管理隔离开来，使得代码发布变得简单，一次打包可以发布到不同的环境，同时修改配置不用重启应用就能实时实现。

ConfigX是一个配置管理系统，为应用提供统一的配置管理，不仅提供了简单属性管理，还可以对配置文件进行管理。

ConfigX包括configx-web（配置管理中心）和configx-client（配置客户端库）。


ConfigX提供以下功能：
1. 配置外部化，将配置与代码分离，由配置管理系统统一管理配置。
2. 配置热修改，在配置管理系统中修改配置，不用重新发布代码，也不用重启应用即可实时生效。
3. 配置版本控制，跟代码版本控制类似，我们对配置也就行了版本控制，可以查看配置的历史修改记录。
4. 多种发布模式，我们提供两种发布模式，自动发布和审核发布，自动发布是指配置修改完立刻自动发布，配置实时生效；审核发布模是指配置修改完后，并不立刻发布，而是需要建立一个发布单，发布单审核通过后，才能发布，审核发布模式可以实现更安全可控的发布，减少配置错误导致的严重后果的风险。
5. 配置继承机制，应用和环境两个维度是为了隔离不同的配置集，为了解决配置继承问题，增加了Profile维度，每个环境下的配置可以分配到不同的Profile下。
[维度设计](https://github.com/zouzhirong/configx/wiki/configx%E7%BB%B4%E5%BA%A6%E8%AE%BE%E8%AE%A1)
6. 配置的原子性，在客户端中实现了多版本的配置管理控制，当发布多个配置时，每个线程看到的这几个配置要么都是修改前的值，要么都是修改后的值，不会出现某些配置是修改后值而另外一些配置是修改前的值，保证配置的原子性。
[多版本控制](https://github.com/zouzhirong/configx/wiki/%E9%85%8D%E7%BD%AE%E7%9A%84%E5%A4%9A%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6)
7. Spring属性无缝迁移到配置管理系统中，在Spring中配置的属性源可以直接将属性文件迁移到配置管理系统中，并不需要修改任何@Value注入的代码。
8. Spring国际化消息无缝迁移到配置管理系统中，在Spring中配置的国际化消息文件迁移到配置管理系统中，并不需要修改任何获取多语言消息的代码。



#### 技术支持
ConfigX官方QQ技术支持群：242310272    
ConfigX官方钉钉技术支持群：11790023
