# Docker Commands

https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes

## `container`

Run a container from an image

```
docker run -dp 5000:80 --name=db redis
```

- `-d` - run the container in detached mode (run in background)
- `-a` - run the container in attached mode (run in foreground)
- `-p 5000:80` - map port 80 of the host to port 5000 in the container
- `--name=db` - the name of the container
- `redis` - the image to use
- `-i` - interactive mode
- `-t` - pseudo terminal

List all running containers and their information

```
docker ps
```

List all running and previously stopped containers

```
docker ps -a
```

Stop a container

```
docker stop <container-name>
```

Remove a container

```
docker rm <container-name>
```

## `image`

Build an image

```
cd webapp
docker build -t webapp .
```

List images

```
docker images
```

Get image information e.g., environment variable

```
docker image inspect <image-name>
```

Remove an image

```
docker rmi <image-name>
```
