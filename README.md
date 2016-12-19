Docker
=======

### Install Docker for Rhel  Linux :
[Docker for Rhel](https://docs.docker.com/engine/installation/linux/rhel/)

### Some usefull links  
[Docker jumpstart](http://odewahn.github.io/docker-jumpstart/)
[Docker files](https://www.digitalocean.com/community/tutorials/docker-explained-using-dockerfiles-to-automate-building-of-images/)

###Docker Commands for day to day survival

* Docker basic
Instead of every time running sudo we can do sudo bash or create another user .
To check listening ports    nestat  -plnt | grep 'LISTEN' .
docker inspect [container-id]   will give json metadata  use grep on it to search info.
docker network inspect bridge.

* Docker Buid
    docker build -t <targetimagename>  .   ( run from the directeroy where the dockerfile exist)
	
* Docker Run
   docker run -p(src:dest) -d [container-d]  -p portmapping -d  background
   
* Docker container entry/see inside
   opening terminal in container
      docker exec -it [container-id] bash
   opening container stdin/stdout
      docker logs [container-id]
	  
* Docker Remove all images and containers
    Delete all containers
     docker rm $(docker ps -a -q)
    Delete all images
     docker rmi $(docker images -q)
	 
	 
