# bela-tflite

## Overview

This repository allows you to build tflite for the Bela board (BeagleBone Black). Removing the need of building tflite on the device itself.

The Dockerfile used in this repo is based on this other one https://github.com/rodrigodzf/bela-torch and https://github.com/XavierGeerinck/Jetson-Linux-PyTorch

## Requirements

- Docker
- A computer with a decent CPU

## Building PyTorch

### Prerequisites

None

### Building PyTorch

After our prerequisites are done, we can compile PyTorch by starting up the docker build process:

```bash
docker buildx build --progress=plain --output type=local,dest=./tflite-install --file Dockerfile.bela .
```

## NB

This repository builds and packs the binaries of tflite, however it does not build a .whl

## References

Thanks a lot to the code repositories and authors below:

* https://github.com/XavierGeerinck/Jetson-Linux-PyTorch
