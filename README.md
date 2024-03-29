# Iagon Compute CLI (Test Node)
Iagon Compute Node CLI is a CLI application which allows users to share their computational power on the Iagon network to earn rewards.

## Introduction
This document provides step-by-step instructions to help you install and set up Iagon Compute Node CLI on your system. Currently only Linux based OS are supported.

## Installation
You can download the Official Compute Node CLI binary from the [Iagon's Github Release page](https://github.com/Iagonorg/Computing-CLI/releases).
Once downloaded, navigate to the CLI binary and mark it as executable:
```bash
chmod +rwx ./iag-cli-linux
```

Iagon Compute Node depends on 3rd party trusted packages to perform various benchmarks. These benchmarks help track the current performance and availability of the node in the Iagon Network for use.
These packages don't come bundled with the Iagon Compute Node CLI binary and have to be installed by the user.
 
### Prerequisites
Before installing the Compute Node CLI, ensure the following prerequisites are met:

#### port forwarding
Enable port forwarding for both ssh server and the compute node binary on a static ip. These ports are to be provided during registration process and should be accessible from the internet.

#### Openssh Server
OpenSSH Server is required for remote access of Compute Nodes. If not already installed, you can install it via apt:
```bash
sudo apt install openssh-server
```
After the installation, ensure that openssh server is running. The user is prompted to provide the ssh port and user credential duing the registration process from the CLI. For testing it is recommended to create a separate ssh user with minimum/restricted permissions.

#### FIO
FIO is a powerful tool for testing I/O performance. Follow the installation instructions from [FIO's Github repository](https://github.com/axboe/fio), or install it via apt:
```bash
sudo apt install fio
```

#### sysbench
Sysbench is a versatile benchmarking tool for evaluating system CPU and memory performances. Installation instructions can be found on [sysbench's Github repository](https://github.com/akopytov/sysbench), or you can install it via apt:
```bash
sudo apt install sysbench
```

## Usage
Once the binary and the necessary dependencies are installed, you can use the Compute Node CLI. There are various commands available in the CLI to make the on-boarding/registration process easier. The user can start the node and execute various test commands to check the hardware status of the node.

### Commands
Execute the following commands, as: `./iag-compute-cli some-command`
1. **start**

    Evaluate/Register the host machine as compute node or start compute node if already evaluated.
2. **stop**

    Stop compute node (if already running)
3. **status**
    
    Check running status of compute node
4. **check**
    
    Check if the system adhere to prerequisite criteria
5. **info**

    Extract basic information about the system
6. **test-node**
    
    Test if the node is accessible from the internet
7. **clear-config**
    
    Clear the configurations
8. **benchmark-memory**
    
    Run memory tests and benchmark for the host machine
9. **benchmark-cpu**
    
    Run cpu tests and benchmark for the host machine
10. **benchmark-storage**
    
    Run storage i/o tests and benchmark for the host machine
11. **benchmark-network**
    
    Run network tests and benchmark for the host machine
12. **help**

    Display help for command
