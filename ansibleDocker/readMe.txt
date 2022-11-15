    1. Difference between VM (Virtual Machine) and Container? VMs are heavywait but Containers are lightweight
    2. Lightweight means easy to deploy, migrate and test 
    3. Each VM use their own OS, Containers can use only single OS 
    4. Microservices --> Loosely couple apps vs tightly coupled apps 
    5. Microservices are Loosely coupled apps --> easy to detect the bugs, easy to fix. 
    6. In Microservices --> AppA, AppB and AppC --> If AppB fails AppA and AppC won't fail. Its totally 
    opposite in legasy apps (tightly coupled apps)
    7. tightly coupled apps called monolithic app.  

    Greatest candidate for Microservices is container. 
    1. Container runtimes -->  Docker, Rocket. Docker is the most famous and we will only learn Docker. 

Configure docker 

1. EC2 vm spin up 
2. sudo su - 
3. yum install docker -y 
4. docker images --> Will fail 
5. service docker status --> returns inactive (dead)
6. service docker start 
7. create docker hub account --> https://hub.docker.com/
8. search box look for tomcat image 
9. docker pull tomcat
10. Docker container can run in 2 modes --> 1) Foreground and 2) detached 
11. Foreground --> docker run --name tomcat-container -p 8080:8080 tomcat:latest --> If proccess is canceled docker container will die 
12. Detach --> docker run -d --name tomcat-container-1 -p 8081:8080 tomcat:latest
13. List docker containers --> docker ps 
14. List all container icluding exited containers --> docker ps -a 
15. docker container ls or docker container ls -a
16. Remove container --> docker stop container-name or id --> docker rm container-name or id
17. Remove image --> docker rmi image name or image id 
18. Dockerfile --> Is a definition for docker image 