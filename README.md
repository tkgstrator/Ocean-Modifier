# Ocean-Modifier

Splatoon 2 Salmon Run seed modifier

## Requirements

- DevkitA64
- Unix like operating system(Ubuntu, macOS)
  - Recommend WSL2 on Window10/11
  - 
### Get Started for Ubuntu on WSL2

### Get Started for macOS

```sh
$ wget https://github.com/devkitPro/pacman/releases/download/v1.0.2/devkitpro-pacman-installer.pkg
$ sudo installer -pkg devkitpro-pacman-installer.pkg -target /
```

#### Install DevkitA64

```sh
$ sudo dkp-pacman -Sy
$ sudo dkp-pacman -Syu
$ sudo dkp-pacman -S switch-dev
```

#### Edit environment variables

`vi ~/.zshrc`

```sh
export DEVKITPRO=/opt/devkitpro
export DEVKITARM=/opt/devkitpro/devkitARM
export DEVKITPPC=/opt/devkitpro/devkitPPC
```

For applying above settings without relaunch the console, input following command and press enter.

`source ~/.zshrc`

#### Clone the project

```sh
$ git clone https://github.com/container1234/Ocean-Modifier
$ cd Ocean-Modifier
$ git submodule update --init --recursive
```

#### Build

```sh
$ make
main.cpp
dmntcht.c
linking Ocean-Modifier.elf
built ... Ocean-Modifier.nacp
built ... Ocean-Modifier.ovl
```

## How to use

### Requirements

- [nx-ovlloader](https://github.com/WerWolv/nx-ovlloader/releases/tag/v1.0.6)
- [Tesla-Menu](https://github.com/WerWolv/Tesla-Menu/releases/tag/v1.1.4)

Copy files to the following directory path.

```
.
├── atmosphere
│   └── contents
│       └── 420000000007E51A
│           ├── toolbox.json
│           ├── exefs.nsp
│           └── flags
│               └── boot2.flag
├── config
│   └── ocean
│       └── config.json
└── switch
    └── .overlays
        ├── ovlmenu.ovl
        └── Ocean-Modifier.ovl
```

### Config.json

```json
{
    "event": [
        0,
        0,
        0
    ],
    "seed": 1234567890,
    "tide": [
        2,
        2,
        2
    ]
}
```
