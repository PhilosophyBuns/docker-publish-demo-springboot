FROM java:8
VOLUME /tmp
ADD demo-0.0.1-SNAPSHOT.jar app.jar
RUN sh -c 'touch /app.jar'
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

EXPOSE 8080
ENV JAVA_OPTS=""
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -Djava.security.egd=file:/dev/./urandom -Dfile.encoding=UTF-8 -jar /app.jar" ]
