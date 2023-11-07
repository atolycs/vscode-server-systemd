# Visual Studio code Systemd Unit file

Visual Studio code Systemd Unit file (Unofficial)

# Features
* Port: `8000`

* Listen: `0.0.0.0`

# Install

* Get VSCode CLI
[here](https://code.visualstudio.com/download)

```shell
$ tar xvfz vscode_cli_alpine_x64_cli.tar.gz
$ sudo cp code /usr/local/bin/code-cli
```

* Install User unit

```shell
$ git clone https://github.com/atolycs/vscode-server-systemd.git/ --depth=1 
$ cd vscode-server-systemd
$ mkdir -p ${HOME}/.config/systemd/user
$ cp vscode-server.service ${HOME}/.config/systemd/user
$ systemctl --user daemon-reload
```

* Start server

```shell
$ systemctl --user enable vscode-server.service
$ systemctl --user start vscode-server.service
```
