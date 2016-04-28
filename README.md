# gabrielrezzonico/docker-ionic

Dockerfile to create a Docker container image to develop ionic apps. Android or Ios SDK Not installed. 

## Docker image user and group

See the dockerfile in gabrielrezzonico/docker-debian

## nvm, node, and npm versions

See the dockerfile in base image: gabrielrezzonico/docker-node

## Run


```bash
docker run --rm -it \
                -v $HOME/workspace/docker-ionic/test_project:/home/docker-user/workspace/docker-ionic/test_project \
                -w /home/docker-user/workspace/docker-ionic/test_project \
                -p 8100:8100 -p 35729:35729 \
                 gabrielrezzonico/docker-ionic
```

For example you can create a new ionic project:

```bash
docker-user@a8164c44664c:~/workspace/docker-ionic$ ionic start test_project sidemenu .
docker-user@a8164c44664c:~/workspace/docker-ionic$ cd test_project
docker-user@a8164c44664c:~/workspace/docker-ionic/test_project$ ionic serve
```
Open http://localhost:8100/ on a host browser. 

## Extra packages

The following packages are installed (on top of the base image):

> * ionic
> * cordova
> * bower
> * grunt
> * gulp
