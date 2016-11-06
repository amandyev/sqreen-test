# sqreen-test

This project starts a tomcat in a docker container. Tomcat will automaticaly add a custom header to all HTTP responses. Any .war file present in the current directory will be deployed.

1. Build docker image
`docker build -t ama/tomcat-sqreen .` 

2. Start docker image
`docker run -p 8080:8080 ama/tomcat-sqreen`

3. Access a resource on localhost:8080
`curl -I http://localhost:8080/any-random-app/`

You should be able to see "X-Instrumented-By: sqreen".
