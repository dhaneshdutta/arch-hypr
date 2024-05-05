### 🪧🪧🪧 ANNOUNCEMENT 🪧🪧🪧
- This Repo does not contain Hyprland Dots or configs! Dotfiles can be checked here [`Hyprland-Dots`](https://github.com/JaKooLit/Hyprland-Dots) . During installation, if you opt to copy installation, it will be downloaded from that centralized repo.
- Hyprland-Dots use are constantly evolving / improving. you can check CHANGELOGS here [`Hyprland-Dots-Changelogs`](https://github.com/JaKooLit/Hyprland-Dots/wiki/Changelogs) 
- Since the Hyprland-Dots are evolving, some of the screenshots maybe old

> [!IMPORTANT]
> install a backup tool like `snapper` or `timeshift`. and Backup your system before installing hyprland using this script. This script does NOT include uninstallation of packages

> [!NOTE]
> Main reason why I have not included an uninstallation script is simple. Some packages maybe already installed on your system by default. If I create an uninstall script with packages that I have set to install, you may end up a unrecoverable system. 

> [!WARNING] 
> Download this script on a directory where you have write permissions. ie. HOME. Or any directory within your home directory. Else script will fail

#### 🆕  Prerequisites
- This install script is intended for atleast Server type / Minimal Arch Linux installed.

#### 🔘 Pipewire and Pipewire audio
- This script will install pipewire and will also disable or will uninstall pulseaudio. If you dont want it, you can simply just delete pipewire.sh in install-scripts folder before installing. 

#### ✨ Costumize the packages to be installed
- inside the install-scripts folder, you can edit 00-hypr-pkgs.sh. Care though as the Hyprland Dots may not work properly!
- default GTK theme if agreed to be installed is Tokyo night GTK themes (dark and light) + Tokyo night SE icons

#### 💫 SDDM and GTK Themes offered
- If you opted to install SDDM theme, here's the [`LINK`](https://github.com/JaKooLit/simple-sddm-2)
- If you opted to install GTK Themes, Icons and Cursor offered are Tokyo Nights. [`LINK`](https://github.com/JaKooLit/GTK-themes-icons) & Bibata Cursor Modern Ice 

#### 👀 NVidia GPU Owners.
- By default, nvidia-dkms will be installed. and only supports GTX 900 and newer. If required to install older driver, edit the nvidia.sh in scripts-folder
> [!IMPORTANT]
> If you want to use nouveau driver, choose N when asked if you have nvidia gpu. This is because the nvidia installer part, it will blacklist nouveau. Hyprland will still be installed but it will skip blacklisting nouveau.
- After installation, check [`THIS`](https://github.com/JaKooLit/Hyprland-Dots/wiki/Notes_to_remember#--for-nvidia-gpu-users)

#### ✨ to run
> clone this repo (latest commit only) to reduce file size download by using git. Change directory, make executable and run the script
```bash
git clone --depth=1 https://github.com/JaKooLit/Arch-Hyprland.git ~/Arch-Hyprland
cd ~/Arch-Hyprland
chmod +x install.sh
./install.sh
```

<p align="center">
    <img align="center" width="100%" src="https://raw.githubusercontent.com/JaKooLit/Arch-Hyprland/main/Installer.png" />

#### ✨ for ZSH and OH-MY-ZSH installation
> installer should auto change your default shell to zsh. However, if it does not, do this
```bash
chsh -s $(which zsh)
zsh
source ~/.zshrc
```
- reboot or logout
- by default agnoster theme is installed. You can find more themes from this [`OH-MY-ZSH-THEMES`](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)
- to change the theme, edit ~/.zshrc . Look for ZSH_THEME="desired theme"

#### ✨ TO DO once installation done and dotfiles copied
- ~~if you opted to install gtk themes, to apply the theme and icon, press the dark/light button (beside the padlock). To apply Bibata modern ice cursor, launch nwg-look (GTK Settings) through rofi.~~ Hyprland-Dots v2.1.18, initial boot file will attempt to apply GTK themes,cursor, and icons. You can tweak more using nwg-look (GTK-Settings) utility
