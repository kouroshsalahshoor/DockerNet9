# Docker
## Images
### Sql server (official image)
- on docker hub search for: microsoft
- find mssql-server https://hub.docker.com/r/microsoft/mssql-server
- go to "How to use" section"
- 2022 image
````
docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=yourStrong(!)Password" -p 1433:1433 mcr.microsoft.com/mssql/server:2022-latest
````
- open SSMS and login to server
- sql login
- server name: localhost,1433
- pwd should not be too short ...
### create an image from a container
````
docker commit <container id> <image name>
````
## Containers
### Shell access
````
docker exec -it <container id> <<command>|bash|ls>
````
#### install vim inside the container
````
apt-get update && apt-get install -y vim
````
### log
````
docker logs <container id>
````
### Running a container deattached
````
docker run -d -p 80:80 nginx
````
### container attached
````
docker attach <container id>
````
### Port mapping
````
docker run -p 80:80 nginx
````
http://localhost/
````
docker ps
docker ps -a
````
### Stopping a container
````
docker stop <container id>
````
### Removing a container
````
docker rm <container id>
````
### removing a running container
````
docker rm -f <container id>
````
### nginx
https://hub.docker.com/_/nginx
````
docker run nginx
````
## Installation
### Hello world - Testing the installation
https://hub.docker.com/_/hello-world
````
docker run hello-world
````
### Docker Cli
must have docker desktop running
### Docker hub
https://hub.docker.com/
### Download Docker desktop
https://www.docker.com/

enable hardware virtualization
## Referenses
https://downloadlynet.ir/2024/01/130360/07/from-zero-to-hero-docker-for-developers/14/
