# Steps for Installing Spring Tool Suite

### Step 1: Download the Spring Tool Suite tarball for Linux, from the [Spring tools](https://cdn.spring.io/spring-tools/release/STS4/4.23.1.RELEASE/dist/e4.32/spring-tool-suite-4-4.23.1.RELEASE-e4.32.0-linux.gtk.x86_64.tar.gz) webpage.
> [check officail website of sprint tools](https://spring.io/tools)

### Step 2: Navigate to dir Download and extract spring tool file
```
cd ~ && cd Downloads
```
 - extract file `tar`
```
tar -xzf spring-tool-suite-4-4.23.1.RELEASE-e4.32.0-linux.gtk.x86_64.tar.gz
```
what is -xzf
 - x : extract the `tar`
 - z : verbose output of the extracting process
 - f : tar archine name

### Step 3: Move file tar after extract to `/opt/sts/` folder, but we need to create `sts` folder in `/opt` folder.
Change dir to `/opt` and create new dir name `sts` in `/opt`
```
cd /opt && mkdir sts
``` 
How to move file from `Download` dir to new folder `/opt/sts`
```
cd Downloads && sudo mv sts-4.23.1.RELEASE/ /opt/sts/ 
```

### Step 4: Creating soft link to launch using terminal
befor create link, we can check all file status in current dir
```
cd /opt/sts/sts-4.23.1.RELEASE/ && ls
```
than
```
sudo ln -sf /opt/sts/sts-4.23.1.RELEASE/SpringToolSuite4 /usr/bin/
```
what `-sf`
 - s : make symbolic link
 - f : remove exiting entries.


### Step 5: Launhing/open STS `Spring Tools Suite` with terminal
[!NOTE] we can launch from any where on `Ubuntu` machine
```
cd Downloads && SpringToolSuite4
```

### Step 6: Create STS shortcut app on Ubuntu
run this command for create file config.
[!NOTE] after run the command `sudo nano ...` it will be show in nano page
```
sudo nano /usr/share/applications/SpringToolSuite4.desktop
```
> In nano we need to add some config like this 
```                 
[Desktop Entry]
# Type app
Type=Application
# Name of app
Name=Spring Tool Suite 4
# Comment with u want
Comment=A customized Eclipse IDE gives a better experience for Spring based Entreprise Applic>
# Path of STS   
Exec=/opt/sts/sts-4.23.1.RELEASE/SpringToolSuite4
StartupNotify=true
Terminal=false
Icon=/opt/sts/sts-4.23.1.RELEASE/icon.xpm
Categories=Development;IDE;Java
```

## After config we can search application on Ubuntu app