mvn package spring-boot:repackage

docker build -t spring-config-server .

if network is not created, do docker network create --driver bridge custom-temp-network

docker run -d -p 8888:8888 --network="custom-temp-network" --name spring-config-server spring-config-server 

