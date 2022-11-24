<h2 align="center"> Windows 10 Pro first setup </h2> 

<h3 align="center"> A checklist for a complete first time setup </h3>

<p align="center">
<img src="https://img.shields.io/badge/Support-Windows%20x64-blue?logo=Windows&style=flat-square">
<img src="https://img.shields.io/github/license/marko-milasinovic/W10_pro_first_setup?style=flat-square">
<img src="https://img.shields.io/github/directory-file-count/marko-milasinovic/W10_pro_first_setup?style=flat-square">
</p>

# Requirements
1) Windows 10 Enterprise Pro image
[Windows Media Creation tool](https://www.microsoft.com/en-us/software-download/windows10) (Freeware) - 
2) USB drive with at least 8GiB, final image file size on flash drive is ~4.8 GiB.


# Installation
After inserting the usb with the windows image, choose Windows 10 Pro (not the "n" version which doesn't have ms media framework)
Decline all privacy promps.


## DefaultApplications

 ```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
* Chocolatey (FOSS) - Software management solution
  * MPV (FOSS) optimised and simple media player | [Manual / wiki](https://mpv.io/manual/stable/#keyboard-control)
```
choco install mpv
```
* [Clementine](https://github.com/clementine-player/Clementine/releases/latest) (FOSS) - A "winamp" style music player
* [GreenShot](https://getgreenshot.org/downloads/) (FOSS) - A screenshot tool
* [qimgv](https://github.com/easymodo/qimgv/releases/latest) (FOSS) - Image viewer
* [KeePass](https://keepass.info/download.html) (FOSS) - light-weight password manager
* [Notepad++](https://github.com/notepad-plus-plus/notepad-plus-plus/releases/latest) (FOSS) - multifunctional code/text editor
* [Revo Uninstaller](https://www.revouninstaller.com/start-freeware-download/) (Shareware) - advanced program uninstaller
* [7-zip regular](https://github.com/mcmilk/7-Zip-zstd/releases/latest) - file archiver with additional functions (eg. hash verification)
* [VLC](https://www.videolan.org/vlc/download-windows.html) (FOSS) - multimedia player and framework
* [Adobe Reader](https://get.adobe.com/reader/download?os=Windows+10&name=Reader+DC+2022.002.20191+English+Windows%2864Bit%29&lang=en&nativeOs=Windows+10&accepted=&declined=mss%2Cmsc%2Ccr&preInstalled=&site=otherversions) (Freeware) - Propriatery pdf reader


## Web browser
* [Google Chrome](https://www.google.com/intl/en/chrome/?standalone=1) (Freeware) - made by Google, based on the Chromium engine
After installing change the following:
Chrome > Settings > System > Continue running background apps when Google Chrome is closed > **OFF**


### Browser extensions
* [UBlock Origin](https://github.com/gorhill/uBlock) (FOSS) - An efficient (ad) blocker for Chromium and Firefox
* [HTTPS Everywhere](https://www.eff.org/https-everywhere/) (FOSS) - encrypts your communications with many major websites
* [ClearUrls](https://gitlab.com/KevinRoebert/ClearUrls) (FOSS) - based on the new WebExtensions technology, automatically removes tracking elements from URLs


## Services
Usefull [wiki](http://revertservice.com/10/) website for Windows 10 service documentation
<p>
Run the following command in *Command Prompt* (as an administrator):

```
sc config XboxGipSvc start= disabled & sc config xboxgip start= disabled & sc config xbgm start=disabled & sc config XblAuthManager start= disabled & sc config XblGameSave start=disabled & sc config workfolderssvc start= disabled & sc config wuauserv start= disabled & sc config WinRM start= disabled & sc config icssvc start= disabled & sc config WMPNetworkSvc start= disabled & sc config wisvc start= disabled & sc config SharedRealitySvc start= disabled & sc config RetailDemo start= disabled & sc config RetailDemo start= disabled & sc config RemoteAccess start= disabled & sc config shpamsvc start= disabled & sc config WFDSConMgrSvc start= disabled & sc config WFDSConMgrSvc start= disabled
```
<p>

