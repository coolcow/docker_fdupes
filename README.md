# farmcoolcow/fdupes

[![](https://img.shields.io/badge/  FROM  -farmcoolcow/entrypoints-lightgray.svg)](https://hub.docker.com/farmcoolcow/entrypoints) [![](https://images.microbadger.com/badges/commit/farmcoolcow/fdupes.svg)](https://github.com/coolcow/docker_fdupes/commits/master) [![](https://images.microbadger.com/badges/image/farmcoolcow/fdupes.svg)](https://microbadger.com/images/farmcoolcow/fdupes) [![](https://images.microbadger.com/badges/license/farmcoolcow/fdupes.svg)](https://raw.githubusercontent.com/coolcow/docker_fdupes/master/LICENSE.txt)

---

## What is fdupes ?

FDUPES is a program for identifying or deleting duplicate files residing within specified directories.. More informations on [the official fdupes github](https://github.com/adrianlopezroche/fdupes).

---

## How to use this image

This image is based on [farmcoolcow/entrypoints](https://hub.docker.com/r/farmcoolcow/entrypoints/).

The default **ENTRYPOINT** is ```/entrypoint-su-exec.sh fdupes``` and the default **CMD** is ```--help```.  

Take a look at [the fdupes README](http://www.harding.motd.ca/fdupes/README) to see all the available parameters.

---

### Example

* Docker-command: 

  ```sh
  docker run -it --rm \
    -e PUID=$(id -u $(whoami)) \
    -e PGID=$(id -g $(whoami)) \
    -v <PATH_TO_YOUR_DATA>:/data farmcoolcow/fdupes \
      -r /data
  ```

  > Replace ```<PATH_TO_YOUR_DATA>``` with the directory-path of your data.

