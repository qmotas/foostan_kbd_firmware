# KBD firmware

## How to build

## 1. Setting Up Your QMK Environment

Please see https://docs.qmk.fm/#/newbs_getting_started and set up 1 to 3.

## 2. Getting source files

Please get source files of `qmk/qmk_firmware` and `vial-kb/vial-qmk`

```sh
make git-submodule
```

## 3. Building firmwares

### for me (qmotas)

```sh
make qmk-clean
kb=cornelius make qmk-init
kb=cornelius kr=rev2 km=qmotas make qmk-compile
```

### for VIA

```sh
make qmk-clean
kb=crkbd make qmk-init
kb=crkbd kr=rev4/standard km=via make qmk-compile
```

A built data will be stored on `keyboards/crkbd/qmk/qmk_firmware/.build`\
Please change `kb`, `kr` and `km` when build other.

### for Vial

```sh
make vial-qmk-clean
kb=crkbd make vial-qmk-init
kb=crkbd kr=rev4/standard km=vial make vial-qmk-compile
```

A built data will be stored on `keyboards/crkbd/vial-kb/vial-qmk/.build`\
Please change `kb`, `kr` and `km` when build other.

### All cleaning and building

```sh
make update-al
```
