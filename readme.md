## 💿 7OS: The Frutiger Aero Kernel

7OS is a custom, bare-metal 32-bit operating system kernel developed from scratch in C and Assembly. It features a nostalgic "Frutiger Aero" graphical aesthetic, a windowing system, and a simulated hierarchical filesystem accessible via a custom shell.
✨ Key Features

    Monolithic Kernel: A bare-metal 32-bit architecture with Multiboot compliance.

    Frutiger Aero GUI: A custom graphical desktop environment with high-resolution 800×600 (VBE) asset support.

    Window Management System: Keyboard-driven window manipulation and UI rendering.

    Dual-Mode Interface: Seamless switching between a glassy graphical shell and a legacy-style Command Line Interface (CLI).

    Resilient Design: Custom interrupt handling and an ASCII-based System Halt (BSOD) routine.

🚀 Deployment & Emulation

The easiest way to experience 7OS is via a Virtual Machine using the provided 7OS.iso.
Method 1: QEMU (Recommended)

If you have the QEMU emulator installed, launch the OS directly from your terminal:
Bash

qemu-system-i386 -cdrom 7OS.iso

Method 2: VirtualBox / VMware

    Create a New VM and name it 7OS.

    Type: Other | Version: Other/Unknown (32-bit).

    Memory: Allocate at least 64 MB RAM.

    Storage: Under Settings > Storage, attach 7OS.iso to the Optical Drive.

    Network/Disk: Not required; 7OS runs entirely in memory.

    Launch: Click Start.

🕹️ User Interface & Navigation

7OS utilizes a command-driven desktop interface. Type the following commands into the global prompt to interact with the system:
Command	Action
explorer	Launches the graphical File Explorer window.
cmd	Switches to the CLI environment (Terminal Green).
info	Displays kernel version and system architecture.
crash	Triggers a manual system halt (for testing handlers).
Window Manipulation

When a graphical window (such as explorer) is active:

    Move: Use W A S D keys to reposition the window.

    Close: Press Q to terminate the process and return to the Desktop.

Command Line Interface (CLI)

Inside the cmd module, the following filesystem operations are supported:

    ls / dir — List directory contents.

    cd <dir> — Change directory.

    mkdir <name> — Create a virtual directory.

    rm <name> — Delete a virtual file/folder.

    exit — Return to the Graphical User Interface.

🛠️ Technical Stack

    Languages: C (90%), x86 Assembly (10%)

    Bootloader: GRUB / Multiboot

    Graphics: VESA BIOS Extensions (VBE)

    Architecture: i386 (Protected Mode)

Note: This project is a functional kernel intended for educational purposes in OS development and low-level systems programming.
