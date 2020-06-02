# Springboot- Eureka Service Discovery- Microservice


Minimal [Spring Boot](http://projects.spring.io/spring-boot/) Sample Eureka Service Discovery service.

## Requirements

For building and running the application you need:

- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3](https://maven.apache.org)

## Building the application locally


To build your app and install dependencies, you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn clean
mvn install
```

## Running the application locally

There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `sa.com.me.eureka` class from your IDE.

Alternatively you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn run
```

## Running the application locally using dockers

### Requirements

install docker daemons on your machine, you can find all the steps here: (https://docs.docker.com/docker-for-mac/)

TO start the application using docker, there is a Dockerfile in the root directory of the application. Navigate to root directory and in your terminal run the following:

```shell
"<path to project directory>/eureka/mvnw" clean -f "<path to project directory>/eureka/pom.xml"
"<path to project directory>/eureka/mvnw" install -f "<path to project directory>/eureka/pom.xml"
docker image build -t eureka-service .
```

That will create your image, then you run your container using:

```shell
docker container run  -it --name eureka -p 8761:8761 -d eureka-service java -jar eureka.jar
```
