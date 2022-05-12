FROM ubuntu:18.04
RUN apt-get update && apt-get install curl openjdk-8-jdk -y
RUN mkdir /server
WORKDIR /server
RUN curl -O https://dlcdn.apache.org/tomcat/tomcat-8/v8.5.78/bin/apache-tomcat-8.5.78.tar.gz
RUN tar -xvf apache*
COPY gameoflife.war /server/apache-tomcat-8.5.78/webapps
EXPOSE 8080
ENTRYPOINT [ "/server/apache-tomcat-8.5.78/bin/catalina.sh", "run" ]

