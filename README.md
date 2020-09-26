# Overview

Lightweight docker image built on top of **debian:jessie-slim** with installed xtensa toolchain, ESP8266_RTOS_SDK and few additional tools:

## ESP8266

* xtensa-lx106 (crosstool-NG crosstool-ng-1.22.0-92-g8facf4c; 5.2.0)
* ESP8266_RTOS_SDK (v3.2)
* ESP8266 Arduino Framework
* esptool.py (v2.4)
* make (v4.2)
* cmake (v3.5)

## ESP32

TBD

## Building image locally

```bash
git clone https://github.com/antonyx/esp-tc-docker.git
cd esp-tc
docker build -f Dockerfile.esp8266 --rm -t esp-tc:8266 .
```

## An example of running toolchain binary

```bash
docker run --rm -it --privileged -v $(pwd):/build esp-tc:8266 xtensa-lx106-elf-gcc --version
```

# Notes

This image is based on the work of lpodkalicki.

