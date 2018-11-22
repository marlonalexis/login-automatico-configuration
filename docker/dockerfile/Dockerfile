FROM openjdk:8-jdk-alpine
RUN mkdir -m 777 /login-automatico-admin
ARG ARTIFACT_VAR
ENV JAVA_FILE=$ARTIFACT_VAR
COPY $JAVA_FILE /login-automatico-admin/$JAVA_FILE
WORKDIR /login-automatico-admin
ENTRYPOINT java -jar -Djava.security.egd=file:/dev/./urandom -Duser.region=EC -Duser.timezone=America/Guayaquil /login-automatico-admin/$JAVA_FILE --spring.config.location=file:/login-automatico-admin/config/application.properties
