# GCC-installing-in-Ubuntu
# GCC Installation Guide (Ubuntu)

This guide explains how to install the GNU Compiler Collection (GCC) on Ubuntu and verify the installation.

## What is GCC?

GCC (GNU Compiler Collection) is a compiler used to compile programs written in C, C++, and other programming languages.

---

## Step 1: Update Package Repository

Open Terminal and run:

```bash
sudo apt update
```

---

## Step 2: Install GCC

Install GCC using:

```bash
sudo apt install gcc -y
```

---

## Step 3: Verify GCC Installation

Check the installed version:

```bash
gcc --version
```

Example Output:

```text
gcc (Ubuntu 13.3.0) 13.3.0
Copyright (C) Free Software Foundation, Inc.
```

---

## Step 4: Install G++ (C++ Compiler)

To compile C++ programs:

```bash
sudo apt install g++ -y
```

Verify installation:

```bash
g++ --version
```

---

## Step 5: Install Build Essential Package

This package includes GCC, G++, Make, and other development tools.

```bash
sudo apt install build-essential -y
```

Verify:

```bash
dpkg -l build-essential
```

---

## Creating and Compiling a Sample C Program

### Create a File

```bash
nano hello.c
```

Add the following code:

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

Save and exit.

---

### Compile the Program

```bash
gcc hello.c -o hello
```

This creates an executable file named:

```text
hello
```

---

### Run the Program

```bash
./hello
```

Output:

```text
Hello, World!
```

---

## Useful GCC Commands

### Compile with Warnings

```bash
gcc -Wall hello.c -o hello
```

### Compile and Debug

```bash
gcc -g hello.c -o hello
```

### Compile Multiple Files

```bash
gcc file1.c file2.c -o program
```

---

## Installed Files Locations

| Component | Location |
|------------|------------|
| gcc executable | /usr/bin/gcc |
| g++ executable | /usr/bin/g++ |
| Libraries | /usr/lib/ |
| Header Files | /usr/include/ |
| GCC Configuration | /usr/lib/gcc/ |

Check GCC path:

```bash
which gcc
```

Output:

```text
/usr/bin/gcc
```

---

## Uninstall GCC

```bash
sudo apt remove gcc g++ -y
sudo apt autoremove -y
```

---

## References

- GCC Official Documentation
- Ubuntu Package Management Guide

---

**Author:** CSE Department  
**Purpose:** GCC Installation and Setup on Ubuntu
