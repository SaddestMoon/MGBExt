## 项目说明 ##

对MyBatis Generator 的一些功能进行了扩展.

## 如何使用 ##

1.下载本项目,打包生成jar.放入本地maven库(maven中央库坐标待完成),命令参考如下:

    mvn install:install-file  -Dfile=D:/jar/MBGExt.jar  -DgroupId=com.aliez  -DartifactId=mbgExt -Dversion=1.0-SNAPSHOT -Dpackaging=jar


2.使用MBG的项目的pom中添加如下依赖:

    <build>
        <plugins>
            <plugin>
        		<groupId>org.mybatis.generator</groupId>
        		<artifactId>mybatis-generator-maven-plugin</artifactId>
        		<version>1.3.2</version>
        		<dependencies>
            		<dependency>
               	 		<groupId>com.aliez</groupId>
                		<artifactId>mbgExt</artifactId>
                		<version>1.0-SNAPSHOT</version>
            		</dependency>
        		</dependencies>
      		</plugin>
        </plugins>
    </build>

3. 在generatorConfig.xml使用MBGExt.例如:
    
	<commentGenerator type="com.aliez.mbgExt.mybatis.generate.internal.CommentGeneratorExt"/>