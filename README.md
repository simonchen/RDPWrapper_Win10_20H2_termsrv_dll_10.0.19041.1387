### I've successfully patched Windows Remote Desktop on Windows Home version (20H2) and this patch is specially for Windows 10 (version 20H2) and who uses termsrv.dll that version is 10.0.19041 (at c:\windows\system32)
# [RDPWrapper_Win10_20H2_termsrv_dll_10.0.19041.1387.zip](https://github.com/simonchen/RDPWrapper_Win10_20H2_termsrv_dll_10.0.19041.1387/blob/main/RDPWrapper_Win10_20H2_termsrv_dll_10.0.19041.1387.zip)

The attached zip file is a customized patch derived from [RdpWrapper](https://github.com/stascorp/rdpwrap)

## How to install the customized RdpWrapper
### 1. It's very simple! you just extract the all files to C:\Program Files\RDP Wrapper\ (if no existing, just manually create it)
then adding 'Network Service' to this folder:

![image](https://user-images.githubusercontent.com/345840/154181634-7d8dd8e3-6cf1-4659-9246-da942dd1ac82.png)

### 2. Open cmd.exe as administrator, then running command as follow
```
C:\Program Files\RDP Wrapper\autoupdate.bat
```
This autoupdate.bat is a customized patch derived from [RdpWrapper - Autoupdater](https://github.com/asmtron/rdpwrap/blob/master/binary-download.md)

What I just changed is to just remain the one link downloading the new rdpwrap.ini for adapting termsrv.dll （10.0.19041.1387）
```
...
set rdpwrap_ini_update_github_1="https://raw.githubusercontent.com/affinityv/INI-RDPWRAP/master/rdpwrap.ini"
...
echo [*] check network connectivity...
:netcheck
...
ping -n 1 baidu.com>nul
...
```

