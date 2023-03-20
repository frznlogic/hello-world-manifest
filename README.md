# README

## Introduction
Repo is a tool for downloading multiple other sources into a structure that the developer defines.
This can then be used to build things that are depending on each other, and it suits yocto perfectly
as you usually have multiple sources that needs to be pulled together.

## Manifests
There are currently the following manifests installed:

none

# Install repo tool

```
$ mkdir ~/bin
$ PATH=~/bin:$PATH
$ curl https://storage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$ chmod a+x ~/bin/repo
```

## How to build common images
This initializes and builds an image that can be used in qemu.

```
mkdir ~/hello-world
cd ~/hello-world
repo init -u git@github.com:frznlogic/hello-world-manifest -b main -m common.xml
repo sync
```

> # Warning
> TBD: Do some manual stuff here that has not been documented yet.

At this point, make sure all the right settings are setup

```
bitbake -k helloworld
```

# hello-world-manifest
