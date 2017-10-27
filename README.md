## to run:

    mvn package && java -jar target/gs-spring-boot-0.1.0.jar

## Create Docker image

    mvn install dockerfile:build

## Start Docker image

    docker run -d --name boot -p 8080:8080 trickito/gs-spring-boot
    curl -v http://localhost:8080/
    
## push to docker hub

    docker login
    docker tag trickito/gs-spring-boot trickito/gs-spring-boot:latest
    docker push trickito/gs-spring-boot:latest
