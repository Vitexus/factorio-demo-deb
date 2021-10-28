![icon](factorio-demo.png?raw=true)

Factorio Demo
=============

Repacked archive from https://factorio.com/download ready to install on Debian & friends.

Installation:
------------

```shell
sudo apt install lsb-release wget
echo "deb http://repo.vitexsoftware.cz $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/vitexsoftware.list
sudo wget -O /etc/apt/trusted.gpg.d/vitexsoftware.gpg http://repo.vitexsoftware.cz/keyring.gpg
sudo apt update
sudo apt install factorio-demo
```

Building
--------

To build current version execute simply:

```shell
debuild -us -uc
```
You can also specify version requested:

```shell 
FORCE_FACTORIO_VERSION=1.1.42 debuild -us -uc
``` 
to repack https://www.factorio.com/get-download/1.1.42/demo/linux64 as deb archive.

See also: https://github.com/factoriommo/factorio-multienv-ctl Full Game packager:  https://github.com/Vitexus/factorio-deb/
