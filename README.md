# ❄️ PT3 - Declarative System Administration with NixOS

## 📌 Description

This project focuses on **declarative system administration using NixOS**, a Linux distribution that introduces a completely different approach to system configuration and management.

Instead of manually installing and configuring software step by step, NixOS allows defining the entire system in a **single configuration file**, making setups reproducible, consistent, and easy to maintain.

---

## 🎯 Objectives

* Understand the concept of **declarative configuration**
* Learn how NixOS differs from traditional Linux distributions
* Manage system configuration using `configuration.nix`
* Work with **Flakes** and **Home Manager**
* Use version control with Git
* Achieve system **reproducibility**
* Deploy and test configurations in virtualized environments

---

## 🧠 Key Concepts

### 🔹 Declarative Configuration

The entire system is defined in a configuration file (`configuration.nix`).
You describe *what you want*, and the system builds it automatically.

### 🔹 Immutability & Atomic Updates

* System changes do not overwrite previous states
* Each update creates a new system generation
* You can roll back to previous versions at any time

### 🔹 Reproducibility

A system can be replicated exactly on another machine by reusing the same configuration files.

---

## ⚖️ NixOS vs Traditional Linux

| Feature            | Traditional Linux            | NixOS                    |
| ------------------ | ---------------------------- | ------------------------ |
| Package Management | Imperative (`apt`, `pacman`) | Declarative              |
| System State       | Mutable                      | Immutable                |
| Updates            | Risk of breaking system      | Atomic & reversible      |
| Reproducibility    | Difficult                    | Guaranteed               |
| File Structure     | Standard (FHS)               | `/nix/store` with hashes |

---

## ⚙️ System Configuration

### 📄 configuration.nix

Main system configuration file where:

* Packages are installed
* Services are enabled
* System behavior is defined

### 🔧 Applying Changes

```bash
sudo nixos-rebuild switch
```

---

## 🧩 Flakes & Home Manager

### 🔹 Flakes

Provide a modern and reproducible way to manage Nix configurations.

### 🔹 Home Manager

Allows managing user-specific configuration without requiring root access.

---

## 🔄 Reproducibility Workflow

* Clone another user's repository
* Adapt hardware configuration
* Modify username if necessary
* Apply configuration using:

```bash
sudo nixos-rebuild switch --flake .
```

---

## 🌐 Version Control

### 🔹 Git Concepts Used

* Repository initialization
* Commits and history tracking
* Branching and merging (conceptually)

### 🔹 Remote Hosting

* Code synchronization using platforms like Codeberg

---

## 🖥️ Virtualization with Proxmox

The project includes deploying NixOS inside a virtualized environment:

* Uploading ISO images
* Configuring virtual machines
* Testing system rebuilds
* Cloning repositories inside the VM

---

## 🧪 Lab Work Includes

* Installing and configuring NixOS
* Managing packages declaratively
* Creating Flake-based configurations
* Synchronizing configurations with Git
* Reproducing environments from other users
* Testing rollback capabilities

---

## 📂 Project Structure

```
PT3-NixOS/
│── configuration.nix
│── flake.nix
│── home.nix
│── README.md
│── documentation.pdf
```

---

## 🛠️ Technologies & Tools

* NixOS
* Nix Package Manager
* Git
* Codeberg
* Proxmox (virtualization)

---

## 👨‍💻 Author

Pol Gautier Alabarce

---

## 📈 Conclusion

This project demonstrates the power of declarative system management.
NixOS enables reliable, reproducible, and maintainable environments, making it a strong choice for modern system administration and DevOps workflows.
