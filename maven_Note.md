# Maven 工具笔记

> maven 犹太语意味着知识的积累，是由Apache基金提供的针对Java平台项目的管理和自动构建工具，涵盖了项目整个周期：编译、测试、报告、打包、安装、部署。



<strong>Maven的下载与安装</strong>:  <a href='https://blog.csdn.net/c_staunch/article/details/100981699?utm_medium=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.control&depth_1-utm_source=distribute.pc_relevant_t0.none-task-blog-BlogCommendFromMachineLearnPai2-1.control'>下载与安装教程</a>

> 配置还系统环境变量后，可以在菜单栏输入`cmd`打开控制台，输入:mvn -version查看是否安装成功



<strong>Maven的目录结构</strong>: ![image-20201225205347491](C:\Users\Sky\AppData\Roaming\Typora\typora-user-images\image-20201225205347491.png)

> bin :含有mvn的运行脚本 

> boot：含有`plexus-classwords`类加载器

> conf：含有`setting.xml`配置文件 

> ​    lib:   含有maven运行时所要的类库

>   maven_repository： 自己创建的本地仓库



<strong>Maven的仓库</strong>

> Maven可以自动管理项目所依赖的`jar`包，在项目较为复杂所需要的`jar`包
>
> 相互依赖并且种类繁多，特别是在项目迁移的过程中管理不便，通过Maven
>
> 可以自动管理这些`jar`包，Maven一共有三个仓库: 本地仓库、私人仓库、中
>
> 心仓库，对项目需要的`jar`包Maven会由近到远的查找：本地->私人->中心
>
> 将需要的包放入本地仓库。 我们通过修稿conf文件中的`setting.xml`配置文件
<localRepository> 本地仓库路径</localRepository> 从而Maven将依赖包每次都
放入自己定义的本地仓库中。



<strong>Maven项目的构建</strong>

> Maven 将项目当作对象 即它的`Project Object Model(POM)` ,采用约定的项目结构，将项目管理看作对: 编译 、测试、打包、安装、部署过程的管理，每一个流程都对应一个mvn命令:
>
> ​                   `mvn  compile/test/package/install/deploy`

项目结构图片:![img](https://pic1.zhimg.com/80/v2-da676cbc15c143dc74ad7de935a3a464_720w.jpg)

![img](https://pic3.zhimg.com/80/v2-1ed8d84dd892e57681c31bd17e4e46e6_720w.jpg)
