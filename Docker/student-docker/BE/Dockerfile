# FROM ubuntu:22.04
# LABEL dev="Anil"

# # Install necessary packages
# RUN apt update -y && \
#     apt install -y unzip default-jdk && \
#     apt clean && \
#     rm -rf /var/lib/apt/lists/*

# # Download and extract Tomcat
# ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.98/bin/apache-tomcat-9.0.98.zip /opt
# RUN unzip /opt/apache-tomcat-9.0.98.zip -d /opt

# # Set up Tomcat and deploy the WAR file
# WORKDIR /opt/apache-tomcat-9.0.98/
# ADD https://docker-compose-anil-buckete.s3.us-east-2.amazonaws.com/student.war /opt/apache-tomcat-9.0.98/webapps/
# ADD https://docker-compose-anil-buckete.s3.us-east-2.amazonaws.com/mysql-connector+(1).jar /opt/apache-tomcat-9.0.98/lib/mysql-connector.jar
# COPY context.xml /opt/apache-tomcat-9.0.98/conf/context.xml

# # Set permissions and run Tomcat
# RUN chmod +rwx /opt/apache-tomcat-9.0.98/bin/*.sh

# CMD ["/opt/apache-tomcat-9.0.98/bin/catalina.sh", "run"]

# EXPOSE 8080

FROM ubuntu:22.04
LABEL dev="Anil"

# Install necessary packages
RUN apt update -y && \
    apt install -y unzip default-jdk && \
    apt clean && \
    rm -rf /var/lib/apt/lists/*

# Download and extract Tomcat
ADD https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.102/bin/apache-tomcat-9.0.102.zip /opt
RUN unzip /opt/apache-tomcat-9.0.102.zip -d /opt

# Set up Tomcat and deploy the WAR file
WORKDIR /opt/apache-tomcat-9.0.102/
ADD https://docker-project-studentapp.s3.eu-north-1.amazonaws.com/student.war  /opt/apache-tomcat-9.0.102/webapps/
ADD https://docker-project-studentapp.s3.eu-north-1.amazonaws.com/mysql-connector.jar  /opt/apache-tomcat-9.0.102/lib/mysql-connector.jar
COPY context.xml /opt/apache-tomcat-9.0.102/conf/context.xml

# Set permissions and run Tomcat
RUN chmod +rwx /opt/apache-tomcat-9.0.102/bin/*.sh

CMD ["/opt/apache-tomcat-9.0.102/bin/catalina.sh", "run"]

EXPOSE 8080