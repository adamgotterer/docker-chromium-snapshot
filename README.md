# Docker Chromium Snapshot Base Image

[DockerHub Repo](https://hub.docker.com/r/chromie/chromium-snapshot/)

This is a base Dockerfile for building containers with a specific Chromium snapshot version. It requires
specifying `--build-args CHROMIUM_REVISION` with the build id of the Chromium snapshot. For example
`--build-args CHROMIUM_REVISION=571375`

A list of Chromium snapshots can be found [here](https://storage.googleapis.com/chromium-browser-snapshots/index.html?prefix=Linux_x64/).

## How to use the base image

```Dockerfile
# Dockerfile
FROM chromie/chromium-snapshot:latest
```

```bash
docker build --build-arg CHROMIUM_REVISION=XXXXX -t my-container .
```
