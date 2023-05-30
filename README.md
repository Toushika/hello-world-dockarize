# hello-world-dockarize Steps written down below : 

**Step-1 : Run the Gradle command using the gradlew.bat script:**

.\gradlew clean build

**Step-2.Create a Dockerfile in Project Directory. The Docker File Content:**

FROM openjdk:11-jdk-slim

WORKDIR /app

COPY build/libs/hello-world-dockarize-0.0.1-SNAPSHOT.jar /app/app.jar

EXPOSE 8080

ENTRYPOINT ["java", "-jar", "app.jar"]

**Make sure to change the  SNAPSHOT.Jar file name on COPY build/libs/**

**Step-3. Build the Docker image using the Dockerfile. Run the following command in the project directory:**

docker build -t hello-world-spring-boot .

**Step-4: Run a Docker container
Run a Docker container using the previously built image. Execute the following command:**

docker run -d -p 8080:8080 hello-world-spring-boot






