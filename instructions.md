Source  
https://github.com/cloudfoundry-samples/spring-music

`git clone https://github.com/cloudfoundry-samples/spring-music.git`

To run locally with Mongo  
`./gradlew tomcatRun -Dspring.profiles.active=mongodb`

To kill running app locally  
`kill $(ps aux | grep 'GradleDaemon' | awk '{print $2}')`

To test  
`curl -X GET --url http://localhost:8080/spring-music/`

To build and distribute .zip and .war  
```shell
./gradlew zipStatic && \
./gradlew war && \
./gradlew copyWar
```

Links  
https://docs.gradle.org/current/userguide/working_with_files.html