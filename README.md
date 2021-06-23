# Basic Docker


[![Docker Base](https://img.shields.io/badge/Docker-Busybox%3A1.33--uclibc%20-green)](https://hub.docker.com/_/busybox)
![Build Size](https://img.shields.io/badge/Build%20Size-1.49%20MB-blue)

This project creates a tiny Docker image that will function as a web server on port 8080 and serve static web assets copied into the image from the site folder.

## Build Container

```
docker build -t basic-docker .
```

## Run Container

```
docker run --rm --init -p 8080:8080 basic-docker
```

Or to run as a daemon

```
docker run -d --init --restart=unless-stopped -p 8080:8080 basic-docker
```
