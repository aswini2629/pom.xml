<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.amazon</groupId>
  <artifactId>helloworld</artifactId>
  <version>1.13</version>
  <packaging>jar</packaging>

  <name>Hello World</name>
  <description>The most basic of Java programssss.</description>
  <url>https://www.coveros.com/</url>
  <inceptionYear>2018</inceptionYear>
  <!-- https://mvnrepository.com/artifact/org.sonarsource.scanner.maven/sonar-maven-plugin -->
<dependencies>
<dependency>
<groupId>org.sonarsource.scanner.maven</groupId>
<artifactId>sonar-maven-plugin</artifactId>
<version>3.2</version>
</dependency>
</dependencies>
<distributionManagement>
   <repository>
      <id>nexus</id>
      <url>http://54.210.173.120:8081/repository/maven-release/</url>
   </repository>
   <snapshotRepository>
      <id>nexus</id>
      <url>http://54.210.173.120:8081/repository/maven-snapshot/</url>
   </snapshotRepository>
</distributionManagement>
<profiles>
<profile>
<id>sonar</id>
<activation>
<activeByDefault>true</activeByDefault>
</activation>
<properties>
<!-- Optional URL to server. Default value is http://localhost:9000 -->
<sonar.host.url>http://35.175.149.45:9000</sonar.host.url>
<sonar.login>4595b26997206afa138a7f86d9643fd1d836a812</sonar.login>  
</properties>
</profile>
</profiles>
  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
    <jdk.version>1.8</jdk.version>

    <maven.compiler.plugin.version>3.8.1</maven.compiler.plugin.version>
  </properties>

  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <version>${maven.compiler.plugin.version}</version>
        <configuration>
          <source>${jdk.version}</source>
          <target>${jdk.version}</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
</project>
