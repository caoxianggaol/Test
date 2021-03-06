# 配置文件
![qi](http://a3.qpic.cn/psb?/V12UM34U0WbQxL/90osI.iQslfAEmVgPvMRoGygtuM8TPseapDqQ*x8oB8!/c/dPIAAAAAAAAA&ek=1&kp=1&pt=0&bo=UwNTA1MDUwMDORw!&vuin=1824857749&tm=1508580000&sce=60-2-2&rf=0-0)
[网易云音乐](http://music.163.com/)听听音乐，放松一下吧。
 ## ehcache.xml
```xml
 <?xml version="1.0" encoding="UTF-8" ?>

<ehcache>
	<diskStore path="d:/myblog/temp" />

	<!-- 如果为true,导致下面两个时间设置无效 -->
	<!-- 闲置时间 最后访问时间 当前时间 -->
	<!-- 存活时间 当前时间 创建时间 -->
	<cache name="nodes" maxElementsInMemory="1" eternal="false"
		timeToIdleSeconds="300" timeToLiveSeconds="300" overflowToDisk="true" />

	<cache name="users" maxElementsInMemory="1" eternal="false"
		timeToIdleSeconds="300" timeToLiveSeconds="300" overflowToDisk="true" />
</ehcache>
```

## logback.xml
```xml
<?xml version="1.0" encoding="UTF-8" ?>
<configuration>
	<appender name="STDOUT" class="ch.qos.logback.core.ConsoleAppender">
		<encoder>
			<pattern>%d{MM-dd HH:mm:ss.SSS} [%thread] %-5level %logger{36} -
				%msg%n</pattern>
		</encoder>
	</appender>
	<root level="debug">
		<appender-ref ref="STDOUT" />
	</root>
</configuration>
```
## pom.xml
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/maven-v4_0_0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<groupId>com.qi</groupId>
	<artifactId>MyBlog</artifactId>
	<packaging>war</packaging>
	<version>0.0.1-SNAPSHOT</version>
	<name>MyBlog Maven Webapp</name>
	<url>http://maven.apache.org</url>
	<properties>
		<logback-version>1.1.7</logback-version>
		<log4j-version>1.2.17</log4j-version>
		<guava-version>19.0</guava-version>
		<gson-version>2.8.0</gson-version>
		<junit-version>4.12</junit-version>
		<taglibs-standard-spec-version>1.2.1</taglibs-standard-spec-version>
		<taglibs-standard-impl-version>1.2.1</taglibs-standard-impl-version>
		<lang3-version>3.6</lang3-version>
		<dbutils-version>1.7</dbutils-version>
		<dbcp2-version>2.1.1</dbcp2-version>
		<servlet-version>3.1.0</servlet-version>
		<codec-version>1.10</codec-version>
		<io-version>2.4</io-version>
		<fileupload-version>1.3.1</fileupload-version>
		<mysql-version>5.1.44</mysql-version>
		<guava-version>23.0</guava-version>
		<slf4j-version>1.7.21</slf4j-version>
		<jsoup-version>1.10.2</jsoup-version>
		<ehcache-core-version>2.4.8</ehcache-core-version>
		<tomcat7-maven-plugin-version>2.2</tomcat7-maven-plugin-version>
		<maven-compiler-plugin-version>3.1</maven-compiler-plugin-version>
	</properties>

	<dependencies>
		<dependency>
			<groupId>net.sf.ehcache</groupId>
			<artifactId>ehcache-core</artifactId>
			<version>${ehcache-core-version}</version>
		</dependency>

		<dependency>
			<groupId>org.slf4j</groupId>
			<artifactId>slf4j-api</artifactId>
			<version>${slf4j-version}</version>
		</dependency>
		<dependency>
			<groupId>ch.qos.logback</groupId>
			<artifactId>logback-classic</artifactId>
			<version>${logback-version}</version>
		</dependency>
		<dependency>
			<groupId>ch.qos.logback</groupId>
			<artifactId>logback-core</artifactId>
			<version>${logback-version}</version>
		</dependency>


		<dependency>
			<groupId>com.google.guava</groupId>
			<artifactId>guava</artifactId>
			<version>${guava-version}</version>
		</dependency>


		<dependency>
			<groupId>org.jsoup</groupId>
			<artifactId>jsoup</artifactId>
			<version>${jsoup-version}</version>
		</dependency>


		<dependency>
			<groupId>commons-fileupload</groupId>
			<artifactId>commons-fileupload</artifactId>
			<version>${fileupload-version}</version>
		</dependency>

		<dependency>
			<groupId>commons-io</groupId>
			<artifactId>commons-io</artifactId>
			<version>${io-version}</version>
		</dependency>

		<dependency>
			<groupId>com.google.guava</groupId>
			<artifactId>guava</artifactId>
			<version>${guava-version}</version>
		</dependency>
		<dependency>
			<groupId>com.google.code.gson</groupId>
			<artifactId>gson</artifactId>
			<version>${gson-version}</version>
		</dependency>
		<dependency>
			<groupId>junit</groupId>
			<artifactId>junit</artifactId>
			<version>${junit-version}</version>
			<scope>test</scope>
		</dependency>
		<dependency>
			<groupId>org.apache.taglibs</groupId>
			<artifactId>taglibs-standard-spec</artifactId>
			<version>${taglibs-standard-spec-version}</version>
		</dependency>
		<dependency>
			<groupId>org.apache.taglibs</groupId>
			<artifactId>taglibs-standard-impl</artifactId>
			<version>${taglibs-standard-impl-version}</version>
		</dependency>

		<dependency>
			<groupId>org.apache.commons</groupId>
			<artifactId>commons-lang3</artifactId>
			<version>${lang3-version}</version>
		</dependency>
		<dependency>
			<groupId>commons-dbutils</groupId>
			<artifactId>commons-dbutils</artifactId>
			<version>${dbutils-version}</version>
		</dependency>
		<dependency>
			<groupId>org.apache.commons</groupId>
			<artifactId>commons-dbcp2</artifactId>
			<version>${dbcp2-version}</version>
		</dependency>
		<dependency>
			<groupId>javax.servlet</groupId>
			<artifactId>javax.servlet-api</artifactId>
			<version>${servlet-version}</version>
			<scope>provided</scope>
		</dependency>
		<dependency>
			<groupId>commons-codec</groupId>
			<artifactId>commons-codec</artifactId>
			<version>${codec-version}</version>
		</dependency>
		<dependency>
			<groupId>mysql</groupId>
			<artifactId>mysql-connector-java</artifactId>
			<version>${mysql-version}</version>
		</dependency>
	</dependencies>
	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.tomcat.maven</groupId>
				<artifactId>tomcat7-maven-plugin</artifactId>
				<version>${tomcat7-maven-plugin-version}</version>
				<configuration>
					<port>80</port>
					<path>/</path>
				</configuration>
			</plugin>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>${maven-compiler-plugin-version}</version>
				<configuration>
					<source>1.8</source>
					<target>1.8</target>
					<encoding>UTF-8</encoding>
				</configuration>
			</plugin>
		</plugins>
		<finalName>MyBlog</finalName>
	</build>
</project>

```