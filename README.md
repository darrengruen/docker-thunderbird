# Thunderbird Dockerized

Docker container to run thunderbird

## Usage

```shell
docker run \
    -d \
    --name thunderbird_"$(date +%s)" \
    -v /home/[username]/.thunderbird:/root/.thunderbird \
    -v /etc/localtime:/etc/localtime:ro \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -e DISPLAY=unix"$DISPLAY" \
    gruen/thunderbird
```
