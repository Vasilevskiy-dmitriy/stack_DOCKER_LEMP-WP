# Instructions.

## Install docker and docker-compose.

```bash
sudo apt-get install docker docker-compose -y
```

## In order to build the env for this project from scratch:
Remove the containers, images, volume from the local machine.
You can clear all the docker stuff: containers, images and it's data using these commands:

```bash
sudo docker rm $(sudo docker stop $(sudo docker ps -a -q)) && \
sudo docker rmi $(sudo docker images -q) && \
sudo docker volume rm $(sudo docker volume ls -q)
```

# Add your user to docker group:

```
sudo usermod -aG docker $USER
```


## Build images & run the containers.

```bash
sudo docker-compose up -d --build
```
## Access the site by URL.

- Dev site URL: http://localhost
