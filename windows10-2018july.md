* mkdir Q:\WINDOWS-SHARE\windows-downloads
* mkdir Q:\WINDOWS-SHARE\windows-documents
* mkdir Q:\WINDOWS-SHARE\linux-downloads

* download from https://download.fedoraproject.org/pub/fedora/linux/releases/27/Spins/x86_64/iso/Fedora-KDE-Live-x86_64-27-1.6.iso
* or https://download.fedoraproject.org/pub/fedora/linux/releases/
* mkdir c:\VMINSTALL and install VmWarPlayer into above dir
* Launch player app and choose th 28-fedora-mate inside c:\VMINSTALL
* Creat VM guest using above ISO use name=Fedora28_mate_2018July21 and  location=C:\VMINSTALL\Fedora28_mate_2018July21 
  * choose Disk size=70GB
  * choose-Customize Hardware, choose Ram=10gb, CPU=6
  
#### Programs install after boot
* Followed https://fastgadgets.info/2018/06/28/things-i-do-after-installing-fedora-28/
* Run Systm Update - takes 15 mins
* Chromium browser – The open source version of the Chrome browser and a great alternative to Firefox.
* Terminator - MultiPanel Terminal
* goto https://www.google.com/chrome/ choose 64 bit rpm

* Change download locations in browser settings

```bash
sudo dnf update -y
sudo hostnamectl set-hostname fastmachine1
sudo dnf install /home/sandhya/Downloads/google-chrome-stable_current_x86_64.rpm
```

* Rhythmbox – My favorite music player.
* Kdenlive – The best open source non-linear video editor in my opinion. It also has the most features.
* Gimp – The best image editor for Linux. It can be too advanced for some, but is certainly feature rich.
* Audacity – A wonderful audio recorder and advanced editor.
* OBS-Studio – A must have tool for any YouTuber or video producer.
* Handbrake – This tool is great for converting video formats if necessary.
```bash
sudo dnf install -y terminator chromium
sudo dnf install -y  rhythmbox kdenlive gimp audacity obs-studio handbrake
```

* I install several gstreamer codecs to play various video files including .mov from Apple products.  If you edit using Kdenlive, you’ll need to install these to support various video file types and containers.

```bash
sudo dnf install gstreamer1-plugin-openh264 gstreamer1-plugins-bad-free gstreamer1-plugins-bad-freeworld gstreamer1-plugins-bad-nonfree gstreamer1-plugins-base gstreamer1-plugins-good gstreamer1-plugins-good-gtk gstreamer1-plugins-ugly gstreamer1-plugins-ugly-free
```
