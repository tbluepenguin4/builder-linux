# Builder GNU/Linux

Builder GNU/Linux is a personal Linux distribution based on Debian 13 (Trixie), designed to be minimal, manual, and optimized for software development. Instead of targeting a wide audience, Builder is built around my own workflow, providing a clean environment with custom tools and scripts that evolve alongside the project.

---
# Goals

- Keep the system lightweight.
- Stay close to Debian.
- Learn how Linux distributions are built.
- Develop custom tools and utilities.
- Document every important design decision.

---

# Project Status
Tested: Not properly
Installable: Untested

------
# Version 0x00
BUILDER GNU/LINUX (0x00 GreenHill)

[SYSTEM IDENTIFICATION]
  - OS Name                  : Builder GNU/Linux
  - Version                  : 0x00
  - Codename                 : GreenHill
  - Distro ID                : builder
  - Base Distribution        : Debian GNU/Linux 13 (Trixie)
  - Hostname                 : builder-live
  - Root Access              : Direct TTY / No Password Required (PAM nullok)

[KERNEL & ARCHITECTURE]
  - Kernel Release           : 6.12.94-1 (2026-06-20) x86_64
  - Kernel Flavor            : SMP PREEMPT_DYNAMIC
  - Architecture             : x86_64 (64-bit)
  - Security Modules         : AppArmor Disabled/Uninstalled (Low Overhead)

[BOOTLOADER & FIRMWARE]
  - Bootloader               : GRUB 2 (Hybrid ISO Structure)
  - Firmware Compatibility   : Dual Boot (Legacy BIOS & UEFI Native x86_64)
  - Kernel Boot Parameters   : boot=live

[REAL-TIME PERFORMANCE & METRICS]
  - RAM Usage (Idle Boot)    : ~177 MiB (out of 1 GB allocated)
  - Available Free RAM       : ~783 MiB
  - Total Installed Packages : 159 packages (dpkg)
  - Running Services         : cron, systemd-journald, systemd-udevd, getty (tty1-6)

[STORAGE & FILES]
  - ISO Image Size           : ~256 MB (268.572.672 bytes)
  - RootFS Tarball Size      : ~237 MB (Gzip Compressed)
  - Uncompressed System Size : ~458 MB
  - Root Filesystem Type     : OverlayFS (tmpfs write layer + squashfs read layer)
  - Loop Devices             : /dev/loop0 (/run/live/rootfs/filesystem.squashfs)
  - /tmp Mount               : tmpfs (nosuid, nodev)

[SOFTWARE & NETWORK]
  - Init System              : systemd (/usr/bin/systemd)
  - Shell Environment        : GNU Bash (/usr/bin/bash)
  - Package Manager          : APT (/usr/bin/apt)
  - APT Repositories         : deb http://deb.debian.org/debian trixie main
  - Network Management       : iproute2 (/usr/sbin/ip)
  - Network Services/DHCP    : dhcpcd & systemd-networkd ready

==================================
------

# Roadmap
[x] Make system bootable
[x] Install GRUB 2
[x] UEFI/Legacy BIOS support
[x] Basic identity
[ ] Advanced identity
[ ] Installable
[ ] Custom commands
[ ] TUI Installer
[ ] Graphical iso installer
[ ] Declarative package files (like NixOS)
[ ] A custom version of fastfetch/neofetch
