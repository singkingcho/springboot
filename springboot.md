# 道一道Spring Boot

## Spring Boot简介

### Spring Boot起源

Spring Boot是2014年单独分离出一个团队开发的基于Spring的一个快速开发j2ee的框架，你是否受够了那些恶心的配置，希望有一天能够早日解脱，嘿嘿嘿，Spring Boot 就是为此而生啊。

### Spring Boot的目标

- 为所有Spring开发提供一个更快，更广泛的入门体验。
- 立即开始斟酌，但随着需求开始偏离默认值，快速避开。
- 提供大型项目（如嵌入式服务器，安全性，指标，运行状况检查和外部配置）通用的一系列非功能性功能。
- 绝对不会生成代码，并且不需要XML配置。

### 环境要求

- JDK8
- Maven3.5以上(虽然不需要这么高，但是请你和我保持一致)
- STS/idea2018(贫道使用idea2018.1.3，建议与我同步)
- Spring Boot2.0.2

==千言万语，不如下海一试啊，我们走，我们走~流浪法师-瑞兹。==

## HelloWorld入门初体验

### 新建Maven工程





### 修改pom.xml

![1527996119529](D:\JY12\springboot\springboot\images\1527996119529.png)



#### 添加父项目

```xml

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.0.2.RELEASE</version>
    </parent>
```





#### 添加web引导依赖

```xml
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>
```





#### 编写一个核心启动类

```java
package com.daodaofun;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.EnableAutoConfiguration;


@EnableAutoConfiguration
public class HelloWorldApplication {

    public static void main(String[] args) {
        SpringApplication.run(HelloWorldApplication.class,args);
    }

}

```





#### 编写一个Controller

```java
package com.daodaofun.controller;


import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.ResponseBody;

import javax.xml.ws.RequestWrapper;

@Controller
public class HelloController {


    @RequestMapping("/hello")
    @ResponseBody
    public String hello() {

        return "Hello World";
    }

}

```





#### 启动测试

直接run main方法即可。







