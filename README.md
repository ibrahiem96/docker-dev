# docker-dev

local development container based on Ubuntu

## How to use

<strong>Turn off VPN before building this image</strong>

1. Clone repo and cd into root dir
2. Run `docker build -t <tag-name> .` to build the image
3. Run `docker-compose up -d ` to start the container
4. Run `docker exec -it <container-name> bash` to exec into container
5. Run `docker-compose down` to shut down the container

## Optional
You can also opt to add aliases that will allow you to start or shut down the container from anywhere

Add the following lines of code to `~/.bash_profile` or `~/.zshrc`

```bash
function updc() { cd ~/workspace/docker-dev; docker-compose up -d; }
function downdc() { cd ~/workspace/docker-dev; docker-compose down; }
function dintoc() { docker exec -it <container-name> bash; }
```
