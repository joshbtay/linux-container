First, install Docker

Then,

```
git clone https://github.com/joshbtay/linux-container.git
cd linux-container
docker build -t linux .
```

You may wish to add this part to your .zshrc or .bashrc:

```
DOCKER_IMAGE_ID="$(docker images -q linux)"
alias linux='docker run -it -v /path/to/host/OS/directory/to/use/for/code/:/code/ $DOCKER_IMAGE_ID'
```

If you restart your terminal, you can run

```
linux
```

and you're in! There should be a directory `/code` that is shared with your host OS.
