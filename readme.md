# Travis Link Checker [![Build Status](https://travis-ci.org/ellerbrock/travis-link-checker.svg?branch=master)](https://travis-ci.org/ellerbrock/travis-link-checker)


![docker](https://github.frapsoft.com/top/docker-security.jpg)

_Check Links in Web documents or Full Websites with Travis CI_

[![Docker Automated Build](https://img.shields.io/docker/automated/ellerbrock/link-checker.svg)](https://hub.docker.com/r/ellerbrock/link-checker/) [![Docker Pulls](https://img.shields.io/docker/pulls/ellerbrock/link-checker.svg)](https://hub.docker.com/r/ellerbrock/link-checker/) [![Quay Status](https://quay.io/repository/ellerbrock/link-checker/status)](https://quay.io/repository/ellerbrock/link-checker/) [![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg)](https://github.com/ellerbrock/open-source-badges/) [![Gitter Chat](https://badges.gitter.im/frapsoft/frapsoft.svg)](https://gitter.im/frapsoft/frapsoft/)

- Docker: [ellerbrock/link-checker](https://hub.docker.com/r/ellerbrock/link-checker/)
- Quay: [ellerbrock/link-checker](https://quay.io/repository/ellerbrock/link-checker)

## Installation

`docker pull ellerbrock/link-checker`

## About the Container

To prevent zombie reaping processes i run [dumb-init](https://github.com/Yelp/dumb-init) as PID 1 which forwards signals to all processes running in the container. 

## Example Usage

`docker run -it ellerbrock/link-checker https://yourdomain.tld`

Please check the [linkchecker](https://github.com/wummel/linkchecker) Repository for further information how to use it.

## Travis CI Configuration

`.travis.yml`:

```
sudo: false

language: bash

services:
  - docker

# Install the Docker Container
install:
  - docker pull ellerbrock/link-checker

# Add your Site or Files to Check
script:
  - docker run ellerbrock/link-checker https://hub.docker.com/r/ellerbrock/link-checker/

# Notification Setup
notifications:
  email:
    on_success: never
    on_failure: always
```



### Contact / Social Media

_Get the latest News about Web Development, Open Source, Tooling, Server & Security_

[![Github](https://github.frapsoft.com/social/github.png)](https://github.com/ellerbrock/)[![Docker](https://github.frapsoft.com/social/docker.png)](https://hub.docker.com/u/ellerbrock/)[![npm](https://github.frapsoft.com/social/npm.png)](https://www.npmjs.com/~ellerbrock)[![Twitter](https://github.frapsoft.com/social/twitter.png)](https://twitter.com/frapsoft/)[![Facebook](https://github.frapsoft.com/social/facebook.png)](https://www.facebook.com/frapsoft/)[![Google+](https://github.frapsoft.com/social/google-plus.png)](https://plus.google.com/116540931335841862774)[![Gitter](https://github.frapsoft.com/social/gitter.png)](https://gitter.im/frapsoft/frapsoft/)
