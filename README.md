# LogAnalyzer application
This is a [Spring Boot](http://projects.spring.io/spring-boot/) application does read, transform an event logger file and persist it in database.
This data can be access through rest end points of this application

## Requirements

For building and running the application you need:

- [JDK 1.8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
- [Maven 3](https://maven.apache.org)

## Building the application locally
You can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
clean install
```

## Running the application 
```shell
Run a Spring Boot application on your local machine. 

To execute the `main` method in the `com.cs.log.analyzer.LogAnalyzerApplication` class from your IDE.
Perform below steps :
1.Go to Run configuration.
2.set program Arguments value as file path :C:\Java_Assignment\LogAnalyzer\logfile.txt <set this path as per availability path>
3.Run the application.


Easy way to run you can use the batch file to run the application.
perform below Steps 

Go to below path and then double click on the below file. (run.bat)
batch file is located on C:\Java_Assignment\LogAnalyzer\run.bat
Application will start

Alternativly also we can run using maven:

mvn spring-boot:run -Dspring-boot.run.arguments="C:\Java_Assignment\LogAnalyzer\logfile.txt"


```

## Accessing application endpoint

Once the application is up, it can be access using endpoint provided in below swagger documentation
Clear browser cache before loading page.

```shell
http://localhost:8080/loganalyzer/swagger-ui/index.html#

http://localhost:8080/loganalyzer/v3/api-docs
```

## Accessing data base
File based database of the application can be access using below end point

```shell
http://localhost:8080/loganalyzer/h2

spring.datasource.url=jdbc:h2:mem:loganalysisdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
```
