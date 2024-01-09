## Description:
Dockerfile for setting up a docker image with the necessary tools to work with AOSP. Useful for allowing multiple people work with the same AOSP source while permitting everyone to put their own overlays and to build their own Android images without having the builds conflict with one another.

## Building the image:
```shell
docker build [path_to_image] -t [image_tag]
```

## Running a container:
```shell
docker run -it --privileged --name [your_container_name] -v /home/devmake/aosp_code/[your_name]:/home/devmake/aosp_build/device/[your_name] -v /home/devmake/aosp_build/:/home/devmake/aosp_build/ [your_image_tag]
```

## Entering the container after exitting it:
```shell
docker start [your_container_name]
docker exec -it [your_container_name] bash
```
