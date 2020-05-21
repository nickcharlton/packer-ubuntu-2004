# packer-ubuntu-2004

An example [Packer][] template for building Ubuntu 20.04 LTS (Focal
Fossa). Ubuntu 20.04 brings with it a new installer, replacing the previous
[Debian installer][1] with [`subiquity`][2].

This is the companion example to my notes on doing this, [_Automating Ubuntu
20.04 installs with Packer_][3].

## Usage

```sh
packer build ubuntu-2004.json
```

## Issues

In case you see the following error, you need to bump the **ssh_handshake_attempts**
```
==> ubuntu-2004: Error waiting for SSH: Packer experienced an authentication error when trying to connect via SSH. This can happen if your username/password are wrong. You may want to double-check your credentials as part of your debugging process. original error: ssh: handshake failed: ssh: unable to authenticate, attempted methods [none password], no supported methods remain
```

In case you see the following error, you need to bump the **ssh_timeout**
```
==> ubuntu-2004: Timeout waiting for SSH.
```

## Author

Copyright (c) 2020 Nick Charlton. MIT Licensed.

[Packer]: https://packer.io
[1]: https://www.debian.org/devel/debian-installer/
[2]: https://github.com/CanonicalLtd/subiquity
[3]: https://nickcharlton.net/posts/automating-ubuntu-2004-installs-with-packer.html
