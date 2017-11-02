# Endpointer build
> A collection of build tools to build, manage and publish endpointer documentation.

[![Docker Build Status](https://img.shields.io/docker/build/developerjack/endpointer-build.svg)]()

## Image

The image is found at [developerjack/endpointer-build](https://hub.docker.com/r/developerjack/endpointer-build/)

## Using the image

Your dockerfile should be based on `developerjack/endpointer-build`.
An example file could be:

```
FROM developerjack/endpointer-build:latest

ADD . /build # Working directory
ADD ./dist /build/public # Hugo output gets put in ./dist in your local FS
RUN ./setup.sh # Assumes you have some type of local build script for your site.

CMD hugo # Invoke hugo. Default output is into /public which is mapped above.
```

## Contributing & Support
Contributions warmly invited. Open an issue or PR to get the conversation started.
Support is best sought via twitter: [@developerjack](https://www.twitter.com/developerjack).

