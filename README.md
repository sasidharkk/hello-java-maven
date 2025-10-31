 Hello Java Maven Project

This project is part of Task 8, which demonstrates how to build and manage a simple Java application using Apache Maven and Jenkins for continuous integration.

📁 Project Structure
hello-java-maven/
│
├── pom.xml
│
└── src/
    └── main/
        └── java/
            └── HelloWorld.java

About the Project

This project contains a simple Java program that prints “Hello, World!” to the console.
The goal is to understand how Maven builds Java projects and how Jenkins automates the build process.

>>>Steps to Build and Run

1. Prepare Project Folder

Create the following structure:

Desktop/
└── hello-java-maven/
    ├── pom.xml
    └── src/main/java/HelloWorld.java

2. Create HelloWorld.java

Path: src/main/java/HelloWorld.java

public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}

3. Create pom.xml

This file tells Maven how to build the project.

<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
         http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.example</groupId>
    <artifactId>hello-java-maven</artifactId>
    <version>1.0-SNAPSHOT</version>
    <build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.8.1</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>
        </plugins>
    </build>
</project>

4. Build with Maven

Open Git Bash or CMD in the project folder and run:

mvn clean package


If successful, you’ll see:

BUILD SUCCESS

5. Setup Jenkins

Start Jenkins locally:

net start jenkins


or via Docker:

docker run -p 8080:8080 jenkins/jenkins:lts


Open Jenkins in your browser: http://localhost:8080

Create a new Freestyle Project

Configure Git (if using GitHub)

Add Build Step → Invoke top-level Maven targets

Command:

clean package

6. Build in Jenkins

Click Build Now
✅ If successful, Jenkins console shows:

BUILD SUCCESS


Take a screenshot of the success message for submission.
<img width="1919" height="1031" alt="Screenshot 2025-10-31 134923" src="https://github.com/user-attachments/assets/b0537e7d-ae49-4609-afc1-36785fe4ddd4" />
<img width="1919" height="1034" alt="Screenshot 2025-10-31 135008" src="https://github.com/user-attachments/assets/dd06da8c-1eed-4c4f-a2e8-9ec5521b7eca" />
<img width="1916" height="1017" alt="Screenshot 2025-10-31 140042" src="https://github.com/user-attachments/assets/e2fdc967-3243-482a-9dee-e2f085cc70ff" />


🖼️ Example Output
Hello, World!

📸 Screenshot

(Below the  your Jenkins build success screenshot here)




🧾 Author

Name: KONDAPANENI SASIDHAR
Task: 8 — Hello Java Maven Project
Course: DevOps Fundamentals
