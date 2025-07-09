to use this runtime ur gonna have to compile it under a linux distribution (or windows)

requirements:

(for linux)
A C compiler (`gcc`), `make` and Simple DirectMedia Layer (SDL2) development packages are required. 

install with:

on RHEL-based distributions (includes Fedora)

```bash
sudo dnf install gcc make SDL2-devel
```

on Debian-based distributions (includes Ubuntu and Mint)

```bash
sudo apt install gcc make libsdl2-dev
```

on Arch-based distributions (includes EndeavourOS, CachyOS and Manjaro) 

```bash
sudo pacman -S gcc make sdl2
```

if ur linux distribution is immutable (such as Fedora Atomic, Bazzite or SteamOS), you can use [Distrobox](https://distrobox.it/). 

Windows:

Visual Studio 2022 or later with the C++ and C development tools installed and vcpkg integration is needed

just run the following commands inside a personal directory. 

```bash
git clone https://github.com/superkitty1549/copy-of-snake
```

```bash
cd copy-of-snake
```

Linux:

```bash
make
```

Windows:

In Visual Studio Developer Command Prompt, run:

```bash
msbuild /p:Configuration="Release"
msbuild /p:Configuration="Release Grayscale"
```

this will produce two binaries — `bf16` and `bf16_grayscale`
the former uses an RGB332 palette, the latter renders in grayscale
test with the programs under `examples/`. Note that `badapple.b` is best used with `bf16_grayscale`.

Example usage:
```bash
./bf16 examples/snake.b
```

```bash
./bf16_grayscale examples/badapple.b
```
