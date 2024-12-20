## Description

This repository provides a patch for VMware Workstation host modules (`vmmon` and `vmnet`) to ensure compatibility with newer Linux kernels on Debian and Ubuntu distributions. It includes automated scripts to build and install the patched modules for seamless integration with your VMware Workstation installation.


## Tested on

- VMware Workstation Pro: Version 17.5.2, 17.6.0, 17.6.1, 17.6.2
- Linux Kernels: Up to version 6.10.x, 6.11.x
- Distributions: Debian-based systems (Debian, Ubuntu, etc.) and Fedora

## Installation
```bash

git clone https://github.com/bytium/vm-host-modules.git
cd vm-host-modules
git checkout 17.6.x

make
sudo make install
```

What will it do?

- Install the compiled `vmmon.ko` and `vmnet.ko` modules to `/lib/modules/$(uname -r)/misc/`.
- Copy the generated `vmmon.tar` and `vmnet.tar` files to `/usr/lib/vmware/modules/source/`.
- Run `vmware-modconfig --console --install-all` to update VMware with the new modules.

## Additional Info

#### Credit: Patch is offered by Jobyer Ahmed

For detailed instruction(share this link if you want to help others with full instruction): https://bytium.com/vmware-workstation-host-module-patch-for-debian-and-ubuntu/

For any technical support and cyber security services contact Bytium - https://bytium.com

For Latest Update Follow Bytium on X: https://x.com/BytiumLLC
