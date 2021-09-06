# OS-Assignment 1
Downloading the latest stable Linux kernel (Linux-5.14.1) from kernel.org, compiling it, and dual booting it with previously installed Linux kernel of version 5.11.0 on a UEFI system running Ubuntu, a Debian based Linux distribution.   
&nbsp;     

### Create a directory
`mkdir os-assignment`    
`cd os-assignment`  
&nbsp;    

### Download the Kernel Source Code
`wget https://cdn.kernel.org/pub/linux/kernel/v5.x/linux-5.6.9.tar.xz`  
&nbsp;    
  
### Extract the Source Codes
`tar -xf linux-5.14.1.tar.xz`  
`cd linux-5.14.1`   
&nbsp;  
   
### Install the Dependencies
`sudo apt-get install build-essential libncurses-dev bison flex libssl-dev libelf-dev`  
&nbsp;  
  
### Configure the Kernel
`cp -v /boot/config-$(uname -r) .config`  
`make olddefconfig`  
&nbsp;  

### Compile the Kernel
`make -j8`  
&nbsp;  

### Install Kernel Modules
`sudo make modules_install`  
&nbsp;    
  
### Install the Kernel
`sudo make install`  
&nbsp;    
  
### Reboot the System
`sudo reboot`  
&nbsp;    
  
### Display System Information
`uname -a`  