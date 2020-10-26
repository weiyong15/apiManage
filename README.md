

*兼容性* 

* 静态页系统暂时只兼容chrome，其他浏览器未测试。
* 后端：jdk1.7 tomcat7  mariadb5.5

## module说明
* xiaoyaoji-web : 小幺鸡web工程
* xiaoyaoji-biz : 小幺鸡业务代码模块
* 其他： 插件目录

## 分支说明
* 默认分支是dev，开发版本的，开发版本的可能会出现编译错误等各种异常情况
* 如果想自己下载编译，请下载其他分支



## 插件开发
* 目前插件类型有导入，导出，文档三种类型
* 可以参照xiaoyaoji-pdf 或者 xiaoyaoji-plugins 模块
### 文档插件
1. 实现cn.com.xiaoyaoji.core.plugin.doc.DocEvPlugin接口
2. 插件目录（采用标准的maven目录结构）
 --- xiaoyaoji-plugins  
 ------ src  
 --------- main  
 -------------- java  
 ------------------ com.xxxxx  
 -------------- plugins-resources  
 ------------------ web （静态页面）  
 ------------------ plugin.json  
3. 打包插件： 采用apache的 maven-assembly-plugin 插件。 具体配置参考已有插件配置
4. 打包方法。 mvn package；



