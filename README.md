# Description
This repository contains source code examples for the ARM Cortex-M3 STM32F103C8T6 microcontroller.

# Dependencies

* arm-none-eabi-gcc
* arm-none-eabi-gdb
* arm-none-eabi-newlib
* openocd (>= 0.8.0)
* make

# How to compile and upload the examples

## Compile
```
$ make
```
You can change the default optimization level (-Og) through the OPT flag:
```
$ make clean
$ make OPT=-O3
```

## Upload / Flash:
Before uploading/flashing/debugging for the first time select the debug adapter:
```
$ ./dbgcfg
Please chose the debug interface:
[0] ST-LINK/V2
[1] ST-LINK/V2-1
[2] JLINK
Choice:
```
After that, your choice will be stored on a local ".interface" file. You can change it at any time by invoking the ```dbgcfg``` script again.

To flash the microcontroller:
```
$ make flash
```

## Clean output files:
```
$ make clean
```

## Generate .bin file:
```
$ make bin
```

## Generate .hex file:
```
$ make hex
```

