# GHDLDocumentation
GHDL needs some tweaks to run on 64bits operating system.

## Set Up
On Ubuntu / Debian like system, install these librairies :

```bash
sudo apt-get install zlib1g-dev lib32z1-dev lib32z1 lib32ncurses5
```

Install the last GHDL version : http://ghdl.free.fr/site/uploads/Main/ghdl-i686-linux-latest.tar

## Usage

In order to use ghdl on a 64bits operating system, we must tell the assembler, the compiler and the linker to use 32bits architecture.

Example with hello world :

```bash
ghdl -a -Wc,-m32 -Wa,--32 --ieee=synopsys hello.vhdl
ghdl -e -Wa,--32 -Wl,-m32 --ieee=synopsys hello_world
```
