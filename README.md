# boot2root
A very basic boot2root machine in docker

## How to use it

Have docker installed on your computer before following the next steps. If it is not installed, install it from here [docker.io](https://www.docker.com/)

After installing docker clone this repository

```
git clone https://github.com/Kaiser784/boot2root.git
```

and run

```
docker-compose up
```

and to get the ip-address of the docker container to start testing run
```
docker container ls #to find the container-id
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <container-id>
```

if you made any changes to the `.yaml` file and want to rebuild the container you can do this

```
docker-compose down
docker-compose up
```
