# Docker-Commands

## Docker Display Commands

- `docker ps`  
    lists all running containers.

- `docker ps -a`  
    lists all containers, including stopped ones.

- `docker images`
    lists all images on the local machine.

- `docker logs <container_id>`
    displays the logs of a specific container.

## Docker Run Commands

- `docker run <image>`  
    runs a container from the specified image.
    mixure of `docker create`, `docker start` and `docker attach`.

- `docker run -d <image>`  
    runs a container in detached mode (background).

- `docker run -p <host_port>:<container_port> <image>`  
    maps a port on the host to a port on the container.

- `docker run --name <container_name> <image>`
    runs a container with a specific name.

- `docker exec -i <container_id> <command>`  
    executes a command inside a running container interactively.

## Docker Build Commands

- `docker build -t <image_name> .`  
    builds a Docker image from a Dockerfile in the current directory.

- `docker build -t <image_name>:<tag> .`  
    builds a Docker image with a specific tag from a Dockerfile in the current directory.

- `docker build --file <Dockerfile_path> -t <image_name> <directory with Dockerfile>`  
    builds a Docker image using a specific Dockerfile.

## Docker Stop and Remove Commands

- `docker stop <container_id>`  
    stops a running container.

- `docker restart <container_id>`  
    restarts a running container.   

- `docker rm <container_id or container_name or image_name or image_id>`  
    removes a stopped container.

- `docker rmi <image_name or image_id>`  
    removes an image by name.

- `docker ps -aq | xargs docker rm`  
    removes all stopped containers.

- `docker ps -aq | xargs docker rm -f`  
    removes all stopped containers and forcefully removes running containers.

## Docker Login Docker Hub

- `docker login`  
    logs into Docker Hub.

- `docker logout`
    logs out of Docker Hub.

## Docker Tagging and Pushing Images

- `docker tag <image_name> <$DOCKER_HUB_USERNAME/app>:<version>`  
    tags an image with a specific repository and tag.

- `docker push <$DOCKER_HUB_USERNAME/app>:<version>`  
    pushes a tagged image to a Docker repository.