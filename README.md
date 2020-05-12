# ksedit

kubernetes secret edit

## install

```bash
# linux
$ curl -L https://github.com/plaidev/ksedit/releases/download/v0.0.5/ksedit_linux_amd64 -o /usr/local/bin/ksedit
$ chmod +x /usr/local/bin/ksedit

# mac
$ curl -L https://github.com/plaidev/ksedit/releases/download/v0.0.5/ksedit_darwin_amd64 -o /usr/local/bin/ksedit
$ chmod +x /usr/local/bin/ksedit
```

## usage

pipe or filepath

```bash
$ cat ./secret.yml | ksedit > ./scret-edited.yml
# or
$ ksedit ./secret.yml > ./scret-edited.yml
```

edit and write

```bash
$ ksedit -w ./secret.yml
```

manually decode and encode

```bash
$ ksedit -d ./secret.yml > ./secret.dec.yml
$ vim ./secret.dec.yml
$ ksedit -e ./secret.dec.yml > ./secret.yml
```

## options

```
USAGE:
   ksedit [global options] filepath

ENVS:
   $EDITOR         (default "vim")

GLOBAL OPTIONS:
   --write, -w     write secret
   --encode, -e    encode secret
   --decode, -d    decode secret
   --help, -h      show help
   --version, -v   print the version
```
