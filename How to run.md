# NexusOS

A lightweight desktop operating system built from scratch, featuring a custom kernel, graphical desktop environment, terminal, window manager, and modular architecture.

---

## Requirements

### Linux / WSL

Install the required development tools:

```bash
sudo apt update

sudo apt install \
nasm \
gcc \
binutils \
grub-pc-bin \
xorriso \
qemu-system-x86 \
make
```

---

# Method 1: Run Using QEMU (Recommended)

This is the fastest way to test NexusOS during development.

## Build the Project

```bash
make clean
make
```

## Create the Bootable ISO

```bash
make iso
```

## Run NexusOS

```bash
make run
```

QEMU will start and boot directly into NexusOS.

---

# Method 2: Run Using VirtualBox

This method allows NexusOS to run as a virtual machine.

## Build the ISO

```bash
make clean
make
make iso
```

After building, you should get:

```text
nexusos.iso
```

or

```text
build/nexusos.iso
```

(depending on the project version).

---

## Create a Virtual Machine

1. Open VirtualBox.
2. Click **New**.
3. Enter the name:

```text
NexusOS
```

4. Set Type:

```text
Other
```

5. Set Version:

```text
Other/Unknown (32-bit)
```

6. Allocate memory:

```text
64 MB minimum
128 MB recommended
```

7. Virtual Hard Disk:

```text
Not Required
```

---

## Attach the ISO

Open:

```text
Settings → Storage
```

Select:

```text
Empty Optical Drive
```

Choose:

```text
nexusos.iso
```

---

## Start the Virtual Machine

Click:

```text
Start
```

GRUB will load and boot NexusOS.

---

# Available Features

Current NexusOS features include:

- Desktop Environment
- Start Menu
- Window Manager
- Terminal
- File Manager
- Memory Manager
- Application Framework
- Modular Architecture

---

# Development Workflow

For everyday development:

```bash
make clean
make
make run
```

This rebuilds and launches NexusOS immediately inside QEMU.

---

# Troubleshooting

## QEMU Error

If you see:

```text
Error loading uncompressed kernel without PVH ELF Note
```

Use:

```bash
make run
```

instead of:

```bash
make run-elf
```

---

## Missing NASM

```bash
sudo apt install nasm
```

---

## Missing GRUB Tools

```bash
sudo apt install grub-pc-bin
```

---

## Missing ISO Builder

```bash
sudo apt install xorriso
```

---

# Project Information

| Item | Value |
|--------|--------|
| Project | NexusOS |
| Architecture | x86 (32-bit) |
| Languages | C, NASM Assembly |
| Build System | GNU Make |
| Bootloader | GRUB2 |
| Virtualization | QEMU, VirtualBox |
| Platform | Linux / WSL |

---

## Built With

C, NASM Assembly, GNU Make, GRUB2, QEMU, Linux, WSL, x86 Architecture, Custom Kernel Development, Custom Desktop Environment, Custom Window Manager, Custom File Manager, Custom Terminal, GNU Binutils, xorriso

---

## License

This project is developed for learning, experimentation, and operating system research purposes.

---

**NexusOS — A lightweight operating system built from scratch, featuring a custom kernel, desktop environment, and terminal.**