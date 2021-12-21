FROM openjdk:11
FROM maven:3.8-jdk-11 as builder

# Copy local code to the container image.
WORKDIR /app
RUN mvn package -DskipTests=true

COPY target/registryserver-*.war  /registryserver.war

EXPOSE 8588

# Run the web service on container startup.
CMD java  -jar /registryserver.war

