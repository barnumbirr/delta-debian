# delta-debian

This repository contains the source to build a Debian package for [delta](https://github.com/dandavison/delta).

## Usage

If you have [Docker](https://www.docker.com/) installed locally, just run the following:

```bash
user@hostname$ ./build.sh
```
By default this will build delta 0.4.0 on Debian Buster.
Since v0.1.1-2 , the package has been renamed `delta-diff` (see discussion in [issue #1](https://github.com/barnumbirr/delta-debian/issues/1)).
The executable is still called `delta` however.

If you want to customize the build at runtime, use the following:

```bash
user@hostname$ ./build.sh -i debian:unstable-slim -v 0.1.1
```
Don't forget to update `debian/changelog` so your package is generated with the correct version.

## Release

To publish a new package version to Github, follow these steps:
  * update the `VERSION` variable in `build.sh`
  * add a new entry in `debian/changelog`
  * create a new tag with the Debian package version

## License

```
Copyright (c) 2020 Martin Simon

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
