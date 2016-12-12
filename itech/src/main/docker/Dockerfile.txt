FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD itech.jar /opt/itech/
EXPOSE 8080
WORKDIR /opt/itech/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "itech.jar"]
