FROM openjdk:8-jdk-alpine

# Add Maintainer Info
#LABEL maintainer="@gmail.com"
RUN mkdir -p /jars

# Add a volume pointing to /tmp
WORKDIR /jar

# Make port 8080 available to the world outside this container
EXPOSE 8080

# The application's jar file
ARG JAR_FILE=meeting-server/target/meeting-0.0.1-SNAPSHOT.jar

# Add the application's jar to the container
ADD ${JAR_FILE} meeting-0.0.1-SNAPSHOT.jar

# Run the jar file
ENTRYPOINT ["java","-jar","/meeting-0.0.1-SNAPSHOT.jar"]
