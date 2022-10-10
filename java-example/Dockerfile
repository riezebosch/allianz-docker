FROM adoptopenjdk/openjdk11 as BUILD
WORKDIR /app
COPY main.java .
RUN javac -verbose main.java

FROM adoptopenjdk/openjdk11:debian-jre
WORKDIR /app
COPY --from=BUILD /app/HelloWorldApp.class .
ENTRYPOINT ["java", "HelloWorldApp"]
