# Managed Application Runtime - Spring Boot Application Example 

This is an example Spring Boot application for Qt Cloud Services - Managed Application Runtime ("**MAR**"). More information about [Spring Boot](http://projects.spring.io/spring-boot/).

## Getting Started

See the Managed Application Runtime getting started documentation at Qt Cloud Services [Developer Documentation ](https://developer.qtcloudservices.com/mar/getting-started)

## Details About This Example

### Procfile

Upon deployed and launched in Cloud Qt Cloud Services the MAR provides an environmental variable **$PORT** for which the HTTP requests from the load balancer port 80 are forwarded into.

## Running and Testing Application Locally

You can start this application from the application root directory with the same following command as declared in the **Procfile** once the project has been built with Maven:


### *nix
```
mvn clean install
java $JAVA_OPTS -Dserver.port=$PORT -jar target/*.jar
```

You may replace the **$PORT** environmental variable with the chosen port number that your local shell process is privileged to run. If the **$PORT** variable is omitted, the HTTP server defaults the port 8080.

### Windows
```
mvn clean install
java -Dserver.port=8080 -jar target\mar-sample-spring-boot-0.0.1-SNAPSHOT.jar
```

Once the server has been started with the default port number, you may test the application with your web browser at address http://127.0.0.1:8080.

## Deploying to Cloud

Please see the Qt Cloud Services [Developer Documentation ](https://developer.qtcloudservices.com/mar/getting-started)

**NOTE**: Without tweaking any command-line Java arguments regarding the heap memory usage deploy the sample app only to the instance which fulfills the following Runtime Size: **ar-1-small (2CU, 512MB)** 