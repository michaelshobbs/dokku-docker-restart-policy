# dokku-docker-restart-policy [![Build Status](https://img.shields.io/circleci/project/michaelshobbs/dokku-docker-restart-policy.svg?branch=master "Build Status")](https://circleci.com/gh/michaelshobbs/dokku-docker-restart-policy/tree/master)

Injects restart policy on [dokku](https://github.com/dokku/dokku) deploy phase

Currently just sets `--restart=on-failure[:10]`.

## requirements

- dokku 0.5.0+
- docker 1.10.x


## installation

```shell
# on 0.5.x
dokku plugin:install https://github.com/michaelshobbs/dokku-docker-restart-policy.git docker-restart-policy
```

## triggers

This plugin provides the following trigger:

* `docker-args-deploy`: adds the `--restart=on-failure[:10]` docker run option to the dokku deploy phase
