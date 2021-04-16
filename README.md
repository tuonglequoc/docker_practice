# Docker Basic

Build image by Dockerfile
-----------
$ docker build -t \<ImageName:Version\> -f \<FolerContainsDockerfile\>

Build docker manually by docker commit
-----------
$ docker run -it \<UbuntuImage\> bash

$ docker commit --change 'CMD["python3", "manage.py", "runserver"]' --change 'EXPOSE 2222' \<ContainerID\> \<ImageName:Version\>

Save image:
-----------
$ docker save \<ImageName\> > image.tar

$ docker save \<ImageName\> -o image.tar

Load image:
-----------
$ docker load < image.tar

$ docker load -i image.tar

Show/Remove images
-----------
$ docker image ls|rm

Show/remove containers
-----------
$ docker ps (-a)

$ docker rm \<ContainerID\>

Run image:
-----------
$ docker run \<ImangeName\>

$ docker run -d (or --detach) -p \<HostPort:ContainerPort\>)

$ docker run -v \<HostDir:ContainerDir\>

$ docker run -e HTTP_PROXY=donkey.cybersoft.vn

$ docker run -it \<ImageName\> bash