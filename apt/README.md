## Linux Package manager
##### Command: 1
```
apt --version
```
**Result:** `apt 2.7.14 (amd64)`

##### Command: 2

```
sudo apt update
```
__Explaination:__
It is required before upgrading the installed packages, because the system cannot know whether the repo has a new version of a package, unless it has an up-to-date copy of the package list.

##### Question: What is the difference between update and upgrade?

__Answer:__
`apt update` updates the package index files, whereas `apt upgrade` upgrades the actual packages installed on your system.
##### Command: 4
```
apt list --upgradable
```
**Result:**

```
base-files/noble-updates 13ubuntu10.2 amd64 [upgradable from: 13ubuntu10.1]
bpftrace/noble-updates 0.20.2-1ubuntu4.3 amd64 [upgradable from: 0.20.2-1ubuntu4.2]
grub-efi-amd64-bin/noble-updates 2.12-1ubuntu7.1 amd64 [upgradable from: 2.12-1ubuntu7]
grub-efi-amd64-signed/noble-updates 1.202.2+2.12-1ubuntu7.1 amd64 [upgradable from: 1.202+2.12-1ubuntu7]
landscape-common/noble-updates 24.02-0ubuntu5.2 amd64 [upgradable from: 24.02-0ubuntu5.1]
libgd3/noble 2.3.3-12+ubuntu24.04.1+deb.sury.org+1 amd64 [upgradable from: 2.3.3-9ubuntu5]
libldap-common/noble-updates 2.6.7+dfsg-1~exp1ubuntu8.2 all [upgradable from: 2.6.7+dfsg-1~exp1ubuntu8.1]
libldap2/noble-updates 2.6.7+dfsg-1~exp1ubuntu8.2 amd64 [upgradable from: 2.6.7+dfsg-1~exp1ubuntu8.1]
libunwind8/noble-updates 1.6.2-3build1.1 amd64 [upgradable from: 1.6.2-3build1]
linux-cloud-tools-common/noble-updates 6.8.0-53.55 all [upgradable from: 6.8.0-52.53]
linux-libc-dev/noble-updates 6.8.0-53.55 amd64 [upgradable from: 6.8.0-52.53]
linux-tools-common/noble-updates 6.8.0-53.55 all [upgradable from: 6.8.0-52.53]
motd-news-config/noble-updates 13ubuntu10.2 all [upgradable from: 13ubuntu10.1]
python-apt-common/noble-updates 2.7.7ubuntu4 all [upgradable from: 2.7.7ubuntu3]
python3-apt/noble-updates 2.7.7ubuntu4 amd64 [upgradable from: 2.7.7ubuntu3]
python3-distupgrade/noble-updates 1:24.04.26 all [upgradable from: 1:24.04.23]
ubuntu-kernel-accessories/noble-updates 1.539.2 amd64 [upgradable from: 1.539.1]
ubuntu-minimal/noble-updates 1.539.2 amd64 [upgradable from: 1.539.1]
ubuntu-release-upgrader-core/noble-updates 1:24.04.26 all [upgradable from: 1:24.04.23]
ubuntu-server/noble-updates 1.539.2 amd64 [upgradable from: 1.539.1]
ubuntu-standard/noble-updates 1.539.2 amd64 [upgradable from: 1.539.1]
```
##### Command: 6
```
apt show gimp
```

**Result:**

```
Depends: libgimp2.0t64 (>= 2.10.36), libgimp2.0t64 (<= 2.10.36-z), gimp-data (>= 2.10.36), gimp-data (<= 2.10.36-z), graphviz, xdg-utils, libaa1 (>= 1.4p5), libbabl-0.1-0 (>= 1:0.1.78), libbz2-1.0, libc6 (>= 2.38), libcairo2 (>= 1.12.2), libfontconfig1 (>= 2.12.6), libfreetype6 (>= 2.2.1), libgcc-s1 (>= 3.3.1), libgdk-pixbuf-2.0-0 (>= 2.30.8), libgegl-0.4-0t64 (>= 1:0.4.38), libgexiv2-2 (>= 0.10.6), libglib2.0-0t64 (>= 2.79.0), libgs10 (>= 9.10~dfsg), libgtk2.0-0t64 (>= 2.24.10), libgudev-1.0-0 (>= 167), libharfbuzz0b (>= 0.6.0), libheif1 (>= 1.13.0), libjpeg8 (>= 8c), libjson-glib-1.0-0 (>= 1.5.2), libjxl0.7 (>= 0.7.0), liblcms2-2 (>= 2.9), liblzma5 (>= 5.1.1alpha+20120614), libmng2 (>= 2.0.2), libmypaint-1.5-1 (>= 1.5.0), libopenexr-3-1-30 (>= 3.1.5), libopenjp2-7 (>= 2.0.0), libpango-1.0-0 (>= 1.29.4), libpangocairo-1.0-0 (>= 1.29.4), libpangoft2-1.0-0 (>= 1.29.4), libpng16-16t64 (>= 1.6.2), libpoppler-glib8t64 (>= 0.44.0), librsvg2-2 (>= 2.32.0), libstdc++6 (>= 13.1), libtiff6 (>= 4.0.3), libwebp7 (>= 1.3.2), libwebpdemux2 (>= 1.3.2), libwebpmux3 (>= 1.3.2), libwmf-0.2-7 (>= 0.2.12), libwmflite-0.2-7 (>= 0.2.12), libx11-6, libxcursor1 (>> 1.1.2), libxext6, libxfixes3, libxmu6 (>= 2:1.1.3), libxpm4, zlib1g (>= 1:1.1.4)
```
##### Command 8
```
apt list --installed | grep gimp
```
**Result:**

```
gimp-data/noble-updates,now 2.10.36-3ubuntu0.24.04.1 all [installed,automatic]
gimp/noble-updates,now 2.10.36-3ubuntu0.24.04.1 amd64 [installed]
libgimp2.0t64/noble-updates,now 2.10.36-3ubuntu0.24.04.1 amd64 [installed,automatic]
```
##### Question: What is the difference between remove and purge?

__Answer:__
Both apt-remove and apt-purge do the same thing and that is to uninstall a package. The apt-purge removes the package and purges any configuration files associated with it.

##### Question: Why `sudo apt autoremove` is important?

__Answer:__
autoremove is used to remove packages that were automatically installed to satisfy dependencies for other packages and are now no longer needed as dependencies changed or the package needing them were removed in the meantime.

##### Question: What does `sudo apt clean` do?

__Answer:__
The clean command clears out the local repository of downloaded package files.

##### Command 13
````
cat /etc/apt/sources.list
````

__Answer:__
This is a list of where the links for apt package manager to find the location of the package repositories to use.