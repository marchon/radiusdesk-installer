RADIUSDesk Installer
====================
## Overview
RADIUSDesk Installer is an [Ansible](http://www.ansible.com) powered utility that attempts to simplify or ease the process of getting a working installation of [RADIUSDesk](http://www.radiusdesk.com) on a vanilla/minimal installation of RHEL/CentOS 6.X/Ubuntu 14.04/15.04/15.10 servers. The Installer utilizes Ansible's powerful features like agentless modes, idempotent runs etc.

## Installation & Usage
1. Clone or download the project.

   a) If you have git already installed, just use `git clone https://github.com/muffycompo/radiusdesk-installer.git`. **Note:** you can install git on RHEL/CentOS 6.x via yum (`yum install -y git`) or Ubuntu via apt (`apt-get install -y git`)
   
   b) If you prefer to download the zip file `wget -cL https://github.com/muffycompo/radiusdesk-installer/archive/master.zip`. **Note:** just make sure you have **wget** and **unzip** installed using (`yum install -y wget unzip`) on RHEL/CentOS 6.x and (`apt-get install -y wget unzip`) on Ubuntu servers.
   
   c) Ensure you have installed python as Ansible requires python to run.
   **Note:** you can install python on RHEL/CentOS 6.x via yum (`yum install -y python`) or Ubuntu via apt (`apt-get install -y python`).
   
   d) SSH into the local/remote server atleast once to have SSH add an entry in its `known_hosts` file. i.e. `ssh localhost` or `ssh 192.168.23.101`
   
   e) Edit the `servers` if you want to customize your server groups. Reference: `http://docs.ansible.com/ansible/intro_inventory.html#hosts-and-groups`
   
2. Run/execute the Installer as **root** or a user with sudo privileges `cd radiusdesk-installer; ./rd-installer` and select I or 1 to commence the installation of RADIUSDesk using default values.
3. Grab yourself a **cup of Coffee** as the installer provisions your server with RADIUSDesk.

4. When the installer is done installing and configuring your system, we recommend rebooting your machine/server to ensure everything is persistent on reboot.

## Features
1. A very customizable installer (Edit `roles/radiusdesk/vars/Debian.yml` or `roles/radiusdesk/vars/RedHat.yml` depending on your Operating System family like Debian, RedHat etc). **Note:** ensure you use a YAML linter to check your syntax anytime you make any change to the variable file(s).

2. Somewhat modularized, so you can always extend RADIUSDesk installer to support your environment

3. Setup PPTPD (Optional)

4. Setup Captive Portal with CoovaChilli (Optional)

## Compatibility
The installer has been tested on the following Linux Operating Systems
 
1. CentOS 6.5/6.7 (32/64 bit)
2. Red Hat Enterprise Linux 6.5/6.7 (32/64 bit) 
3. Ubuntu 14.04/15.04/15.10 (32/64 bit) 

## Resources
1. [RADIUSDesk Course/Tutorials](http://www.maomuffy.com/introduction-to-radiusdesk-with-rhelcentos-6-x-mini-course/) by [Mfawa Alfred Onen](http://ng.linkedin.com/in/mfawaalfredonen/)
2. [RADIUSDesk Project](http://www.radiusdesk.com) by [Dirk van der Walt](http://www.linkedin.com/pub/dirk-van-der-walt/11/b64/79a)
3. [RADIUSDesk Installer Videos](http://www.maomuffy.com/radiusdesk-installer-project/)

## Contributions
1. Anyone is welcome to contribute by sending a pull request with your desired feature tested and implemented.
2. If you have tested the installer in a Linux Distribution that is not in the compatibility list, kindly contact send an email to muffycompoqm[at]gmail[dot]com.

## Copyright and License

Copyright (c) 2016 Mfawa Alfred Onen

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
