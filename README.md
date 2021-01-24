# Docker PHP IDE

Docker image that packages PHP, VSCode, and a few extensions with the goal of becoming a replacement for PHPStorm.

Note: This image has only been tested on Linux.  

Also, the editor is configured to my liking.  If you don't like my configuration feel free to fork this repo and configure to your liking.

# Usage

## Launch the IDE

```console
$ docker run --rm -it -d --privileged -v /tmp/.X11-unix:/tmp/.X11-unix -v $(pwd):/app -e DISPLAY=unix$DISPLAY --device /dev/dri --name php-ide --net="host" mikegeorgeff/vscode:php7.4
```

You can also setup a bash alias

```
vim ~/.bashrc

alias php-ide="docker run --rm -it -d --privileged -v /tmp/.X11-unix:/tmp/.X11-unix -v $(pwd):/app -e DISPLAY=unix$DISPLAY --device /dev/dri --name php-ide --net="host" mikegeorgeff/vscode:php7.4"

source ~/.bashrc
```

## Installed VSCode Extensions

* [PHP IntelliSense](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-intellisense)
* [PHP Debug](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug)
* [Ayu Color Scheme](https://marketplace.visualstudio.com/items?itemName=teabyii.ayu)