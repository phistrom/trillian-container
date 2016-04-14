# trillian-container
A Dockerfile that gets [Trillian Instant Messenger for Linux by Cerulean Studios][trillian] running in a Docker container. 
Available as `phistrom/trillian` on [DockerHub].

## `run` command
```sh
docker run --name trillian -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY -d phistrom/trillian
```

`-v /tmp/.X11-unix:/tmp/.X11-unix` is needed to display the window

## Tips
 * If you quit Trillian, you can relaunch it by just running `docker start trillian`
 * If you close the Trillian window, it will probably still be running and you won't be able to switch back to it. I can only suggest running `docker stop trillian`.

## Issues
 * Can't get audio to work
 * Only tested in Ubuntu Xenial 16.04 Desktop Beta 2

[DockerHub]: <https://hub.docker.com>
[trillian]: <https://www.trillian.im/get/linux/2.0/linux.html>
