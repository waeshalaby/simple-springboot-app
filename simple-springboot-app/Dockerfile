# Use UBI9 as the base image
FROM registry.access.redhat.com/ubi9/ubi:latest

# Install OpenJDK
RUN yum install -y java-11-openjdk && \
    yum clean all
    
# Set the working directory
WORKDIR /app

# Copy the built JAR file into the container
COPY target/simple-springboot-app-0.0.1-SNAPSHOT.jar /app/app.jar

# Expose the application port (adjust if necessary)
EXPOSE 8080

# Command to run the application
CMD ["java", "-jar", "app.jar"]
