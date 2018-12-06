# skicka

## Auth

```terminal
$ docker run --rm -u $(id -u) -e HOME -v skicka:$HOME dmitryrck/skicka init
$ docker run --rm -u $(id -u) -e HOME -v skicka:$HOME dmitryrck/skicka -no-browser-auth ls /
```

Follow the instructions.

## Upload/Download

By default there is no files sharing between your machine and skicka.

If you need to access files in your machine use something like:

```terminal
$ docker run --rm -u $(id -u) -e HOME -v skicka:$HOME -v $(pwd):/data -w /data dmitryrck/skicka upload myfile
```
