# You can change this base image to anything else
# But make sure to use the correct version of Java
FROM adoptopenjdk/openjdk11:alpine-jre
LABEL maintainer="rudresh@singh.com"
# Simply the artifact path
ARG artifact=target/spring-boot-web.jar

WORKDIR /opt/app

COPY ${artifact} app.jar
ENTRYPOINT ["docker", "image", "rmi", "-f", "myapp"]
# This should not be changed
CMD ["java","-jar","app.jar"]
