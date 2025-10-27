## Installation

## About

Trillium is a free, open source web app for robotics.

![Screenshot](./screenshot.png)

## Web

You can run the web version of trillium a number of ways.

1. Visit the Github hosted online page: [https://pdragy.github.io/trillium](https://pdragy.github.io/trillium)
This page will always be running at the tip of the 'main' branch, built and deployed using the github actions defined in the `.github` directory.
2. Run it offline locally, by downloading the packaged site in the Releases section of Github, and serving it on your machine. For example on linux:
```
unzip trillium.zip
python -m http.server 8080 --directory trillium
```
3. Build and run the docker container locally:
```
docker build -t trillium .
docker run --rm -it -p 8080:8080 trillium
```

For 2 or 3, visit http://localhost:8080 in your browser.

For more ways to build and run the code, see CONTRIBUTING.md

## Desktop

In the Releases section in Github, download the latest installer for your platform.
There is not MacOS installer (yet).

To build the Desktop application, see CONTRIBUTING.md

## Extensions

A number of extensions are available and installable directly in your browser or in the Desktop app. To view and manage these, go to Trillium->Settings->Extensions.

## History and related projects

Trillium is a fork of Foxglove, and Foxglove was built/copied from [webviz](https://github.com/cruise-automation/webviz). Last known release of open-sourced Foxglove studio v1 before it was deleted and taken private was 1.87.0, and last commit was [56620d2](https://github.com/pdragy/trillium/commit/56620d28a684503a50f6c793b41b11e968b08254)

Foxglove v1.87.0 is availabile under the [Mozilla Public License v2.0](https://github.com/pdragy/trillium/blob/56620d28a684503a50f6c793b41b11e968b08254/LICENSE).

[Lichtblick](https://github.com/lichtblick-suite/lichtblick) is another fork of Foxglove, maintained by BMW. It became the parent repo of foxglove/studio forks when foxglove/studio commit history was deleted. 

There are many differences between Trillium and Lichtblick. A quick one to note is the size differences, the uncompressed trillium web app is more than 40% smaller than lichtblick's. If you factor out the size of the common base image (caddy:2.5.2-alpine, 45MB) then it is nearly 60% smaller.

### Desktop linux binaries:
- lichtblick-1.20.0-linux-amd64.deb: 99 MB
- trillium-3.0.0-linux-amd64.deb:    76 MB

### Dockerfile (web app):
- ghcr.io/lichtblick-suite/lichtblick   latest    214fdac0f0df   3 weeks ago    189MB
- cloudv0/trillium                      latest    5e89d136d6c4   2 months ago   105MB
