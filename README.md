# Docker Ubuntu

[![Build Status](https://travis-ci.org/petrepatrasc/docker-ubuntu.svg?branch=14.04)](https://travis-ci.org/petrepatrasc/docker-ubuntu)

This repository is a base image that installs some common software required for building some other containers. It essentially allows for the setup of a base Ubuntu image with some defaults that are pre-configured for debug, maintenance and process management.

* [Docker Hub](https://hub.docker.com/r/petrepatrasc/docker-ubuntu/)
* [GitHub](https://github.com/petrepatrasc/docker-ubuntu)

## Usage

In order to run the container you can simply run:

`docker run -it petrepatrasc/docker-ubuntu`

The image is available on Docker Hub for multiple versions of Ubuntu:

* 14.04: `docker run -it petrepatrasc/docker-ubuntu:14.04`
* 15.04: `docker run -it petrepatrasc/docker-ubuntu:15.04`
* 15.10: `docker run -it petrepatrasc/docker-ubuntu:15.10`

## Extending

You can use any of the images above in order to extend and build your own.

    FROM petrepatrasc/docker-ubuntu

    RUN apt-get install -y -qq apache2

    EXPOSE 80

## Software Configured

This image comes pre-configured with the following:

* vim
* cURL
* supervisord
* netcat
