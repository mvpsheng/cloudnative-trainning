# Cloud Native Java Workshop

## 设置
> 微服务，包含很多可移动部件。这个实验就是要尝试去运行这些部件。

- Java 版本最低 Java 8.
- Maven 3.1
- IDE IDEA
- 可以用Spring Boot CLI 或 Spring Cloud CLI 来替换大量代码。
- [下载 Cloud Foundry CLI](https://docs.cloudfoundry.org/devguide/installcf/install-go-cli.html)

## 1. 启动

> 这个实验中要搭建一个Spring Boot 应用 使用JPA 和 Spring Data REST。 学习如何启动一个新项目，SpringBoot如何展示功能，测试是怎么回事，


- 去 [Spring Initializr](http://start.spring.io) 选择 `Web`, `JPA`, `H2`, `Actuator`, `Config Client`, `Eureka Discovery`, `Lombok`, `Zipkin Client`, `Stream Rabbit`, `Cloud Contract Verifier` and `Integration`. 设置`artifactId` of `reservation-service`.
- 点击生成然后解压文件包. Change into the directory of the unzipped project and 运行 `mvn clean install`.
- Open the project in your favorite IDE using Maven import.
- Open `pom.xml` and comment out dependencies that we don't need, for the moment, including: `org.springframework.cloud`:`spring-cloud-starter-stream-rabbit`, `org.springframework.cloud`:`spring-cloud-starter-config`, `org.springframework.cloud`:`spring-cloud-starter-zipkin`, and `org.springframework.cloud`:`spring-cloud-starter-eureka`.
- Add a simple entity (`Reservation`) with an `id` field and a `reservationName` field. Use Lombok to synthesize getters/setters, all-argument and no-argument constructors.
- create a new JPA repository (`ReservationRepository`)
- Observe that we have a Maven wrapper (`./mvnw`) in the build to support reproducible builds
