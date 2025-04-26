
# Ex 01 - Simple Web Server using Spring Boot

## AIM:
To develop a Simple Web Server using Spring Boot that can handle basic HTTP requests and return appropriate responses through RESTful endpoints.

## ALGORITHM:

1. **Start a New Spring Boot Project**  
   Use Spring Initializr (https://start.spring.io/)  
   Select dependencies: `Spring Web`

2. **Create the Main Application Class**  
   This class contains the `main()` method with `@SpringBootApplication` annotation to bootstrap the application.

3. **Create a Controller Class**  
   Create a class annotated with `@RestController`.  
   Define one or more HTTP request handler methods using `@GetMapping`, `@PostMapping`, etc.

4. **Write Endpoint Methods**  
   Inside the controller, define a simple method for handling GET requests (e.g., return “Hello World” when `/hello` is accessed).

5. **Run the Application**  
   Run the application using your IDE or via the command line:
   ```bash
   mvn spring-boot:run
         or
   ./mvnw spring-boot:run
   ```

6.	**Test the Endpoint**
  Open a web browser or use Postman to visit:
  http://localhost:8081/hello
  You should see the output (e.g., “Hello World”).

7.	**Stop the Server**
Stop the Spring Boot server once testing is complete.

⸻

## 📁 Program Structure

simple-web-server/
├── src/
│   └── main/
│       ├── java/
│       │   └── com.example.demo/
│       │       ├── DemoApplication.java
│       │       └── HelloController.java
│       └── resources/
│           └── application.properties
├── pom.xml



⸻

## 📄 pom.xml

```
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>simple-web-server</artifactId>
    <version>0.0.1-SNAPSHOT</version>
    <name>Simple Web Server</name>
    <description>Demo project for Spring Boot Web Server</description>

    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.1.2</version>
        <relativePath/>
    </parent>

    <dependencies>
        <!-- Spring Boot Web -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
</project>
```


## 🚀 DemoApplication.java

```
package com.example.demo;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class DemoApplication {
    public static void main(String[] args) {
        SpringApplication.run(DemoApplication.class, args);
    }
}
```



## 🌐 HelloController.java

```
package com.example.demo;

import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloController {

    @GetMapping("/hello")
    public String sayHello() {
        return "Hello, Spring Boot!";
    }
}
```

## ⚙️ application.properties

server.port=8081



## ✅ Output

Visit http://localhost:8081/hello

Response:
Hello, Spring Boot!

<img width="2168" alt="Screenshot 2025-04-26 at 09 00 54" src="https://github.com/user-attachments/assets/12a88d01-c1bd-45f2-8e25-5eacfa8e1e8c" />
