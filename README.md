# golang-get

`golang-get` is a little script that will fetch the most recent version of
[Go](https://golang.org) for macOS from the [official download
site](https://golang.org/dl) and install it. This may be useful if you do not
use [Homebrew](https://brew.sh) to manage your Go installation. The script will
detect your Mac's architecture and download the correct package for it.

## Installing

Either clone this repository and copy or move `golang-get` to a directory in
your `$PATH`, or change to a directory in your $PATH and run the following
command:

```
curl -OLSs https://raw.githubusercontent.com/ianfoo/golang-get/main/golang-get && chmod 755 golang-get
```

## Running

Simply run the following command:
```
golang-get
```

The script will ask for your password since `/usr/sbin/installer` must be run
with sudo.

If you need a specific version of Go, you can pass it as a command line
argument, like so:

```
golang-get 1.15.12
```

## Dependencies

You will need [HTTPie](https://httpie.io) or [curl](https://curl.se) installed
for this script to work. This shouldn't be a problem since macOS includes curl
in `/usr/bin`.
