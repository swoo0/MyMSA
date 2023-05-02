# dockerfiles-centos-user-adderable
Nginx install

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t swoo0/nginx .
	docker run -d --name w1 -p 8888:80 swoo0/nginx
```
Get the port that the container is listening on:

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        swoo0/nginx      "/bin/bash"         7 seconds ago       Up 6 seconds                            w1
```

To test, ("swoo0" is username. )
```
	open 127.0.0.1:8888
```
To Rollback
```
    docker rm w1 -f
    docker rmi swoo0/nginx
```
