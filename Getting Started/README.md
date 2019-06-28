# 1. create a simple Java project winth maven 
1. Open a command prompt and change the directory to the folder in which you want to create your first Maven project.

2. Run the following command:

    mvn archetype:generate -DgroupId=com.dan.mvn -DartifactId=Simple-project -DarchetpyeArtifactId=Maven-archetype-quickstart -DinteractiveMode=false
3. you will see Maven downloading a bunch of files

4. Then it will start generating sources

5. When Maven has completed generating sources,it will create project that we want

## Let's look the folder structue that is created:
* pom.xml the maven project conifiguration file
* scr \main\java: This is for java source files
* scr \test\java: This is for java test source files
* scr \main\resources: This is for resource for the project 
* scr \test\resources: This is for resource for the test 

插件被放在系统的本地仓库里，一旦下载，再也不用重复下载，除非被删除。
# 2. Building a simple project with maven ，
 
1. Open a command prompt and  run the follwoing command,changing the directly to the folder the project was create:

2. Oberserver the following thing s itn hte output:


3. A jar file file is now created.

## how it work 
 mvn package 
经历了四个生命周期
* validate
* compile 
* Test
* Package

# 3. Change the location of the Maven repository 


maven  配置
# 配置阿里云镜像
```
<mirror>
　　　　<id>alimaven</id>
　　　　<mirrorOf>central</mirrorOf>
　　　　<name>aliyun maven</name>
　　　　<url>http://maven.aliyun.com/nexus/content/groups/public/</url>
　　</mirror>

```
# 配置本地仓库
```
<localRepository>F:\IT_zhengqing\maven\repository-zhengqing</localRepository>
```
# 配置代理服务
```
<!-- proxies
   | This is a list of proxies which can be used on this machine to connect to the network.
   | Unless otherwise specified (by system property or command-line switch), the first proxy
   | specification in this list marked as active will be used.
   |-->
  <proxies>
    <!-- proxy
     | Specification for one proxy, to be used in connecting to the network.
     |
    <proxy>
      <id>optional</id>
      <active>true</active>
      <protocol>http</protocol>
      <username>proxyuser</username>
      <password>proxypass</password>
      <host>proxy.host.net</host>
      <port>80</port>
      <nonProxyHosts>local.net|some.host.com</nonProxyHosts>
    </proxy>
    -->
  </proxies>
```
