This is a template that can be used to stand up a docker project with some best practices involved:

**WIP**
* Volumes for Docker
* Mounting Volumes
* Shared Logs
* Logging in DotNetCore


# Handy Ubuntu Commands

```du -sh .``` - show me the size of this directory


# Handy Docker Commands

## Docker Compose

```docker-compose up --build``` (Build the whole composition and tail)

```docker-compose up --build -d``` (Build the whole composition but don't tail)

```docker-compose run Teamcity.documentreleasenotes.app bash``` (runs just a given app that might have exited, such as the app that populates the release documents)

```docker-compose down``` (Bring down everything and destroy the containers)

```docker-compose up --build --force-recreate``` (Force the built images to not use the currently cached images)

## Docker

```docker ps``` - show all the running containers

```docker images``` - show all the images on the host

```docker rmi _image id_``` - delete an image

```docker exec -it _container id_ bash``` - this command will drop you into your container if it's still running. get the container id from a ps command

```docker container purge``` - purge all stopped containers. You'll need to do this before deleting an image

```docker ps -aq``` - List all containers (only IDs) 

```docker stop $(docker ps -aq)``` - Stop all running containers. 

```docker rm $(docker ps -aq)``` - Remove all containers. 

```docker rmi $(docker images -q)``` - Remove all images. 

From solution directory, if you want build the dockerfiles, you have to do it with a relative path
(e.g - You are at the yaml level, run the following command)

```docker build -t project:latest -f project_folder/Dockerfile .```


# Ubuntu References

**WIP**

# Docker References


[Docker For Windows](https://docs.docker.com/docker-for-windows/)

[Dot Net Docker Samples](https://github.com/dotnet/dotnet-docker-samples)

[Best Practices for Docker Files](https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/)

[Dockerizing with CI AND CD](https://radu-matTeamcity.com/blog/aspnet-core-docker-azure/)

[Sharing Volumes Between Docker Containers](https://www.digitalocean.com/community/tutorials/how-to-share-data-between-docker-containers)

[Docker Compose](https://docs.docker.com/compose/compose-file/)

[DockerFile Docs](https://docs.docker.com/engine/reference/builder/)

[Docker Volumes](https://docs.docker.com/engine/admin/volumes/volumes/)

[Multi-Stage Builds](https://docs.docker.com/engine/userguide/eng-image/multistage-build/)

[Multi-Stage Builds with DOTNET Core](https://hub.docker.com/r/microsoft/dotnet/)

[Dot Net Core and Node JS](https://developers.filiosoft.com/docker/dotnetcore-node)

[Raneto in Docker](https://github.com/appsecco/raneto-docker)

[Multi-Container Application](https://docs.microsoft.com/en-us/dotnet/standard/microservices-architecture/multi-container-microservice-net-applications/multi-container-applications-docker-compose)

[Using Service Name For Referencing Other Containers](https://docs.docker.com/docker-cloud/apps/service-links/#service-environment-variables)

[Docker Compose Networking Explained](https://docs.docker.com/compose/networking/)

[Environment Variables in Compose](https://docs.docker.com/compose/environment-variables/)

[Docker Configs](https://docs.docker.com/engine/swarm/configs/)