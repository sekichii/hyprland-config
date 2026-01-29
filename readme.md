## All requirements
This file contains all dependencies and requirements of the dotfiles.

1. HyprLand specific stuff:
    - `hyprland`
    - `hyprpaper`
    - `hypridle`
    - `hyprlock`
    - `hyprcursor`
2. Wayland utilities:
    - `xdg-desktop-portal-hyprland`
    - `waybar`
    - `wofi`
    - `grim` + `slurp`
    - `wl-clipboard`
3. Audio, Brightness, Network
    - `pipewire` + `wireplumber` + `pipewire-pulse`
    - `brightnessctl`
4. Others
    - `mako`
    - `thunar`
    - `foot`
5. Fonts
    - `noto-fonts`
    - `noto-fonts-cjk`
    - `noto-fonts-emoji`
    - `ttf-jetbrains-mono`

## Final pacstrap
This is the final `pacstrap` I use to install everything I need in Arch.
Note: You might need different modules. This repo is more of a personal backup for myself, **not really intended** as a public dotfile configuration, but the circumstances required me to make the repository public. Please also note that this might have other packages not mentioned above, that I need myself.
```
pacstrap -K /mnt base linux linux-firmware \
        hyprland hyprpaper hypridle hyprlock hyprcursor \
        waybar wofi grim slurp wl-clipboard \
        pipewire wireplumber pipewire-pulse brightnessctl pavucontrol \
        iwd networkmanager \
        mako thunar foot \
        qt5-wayland qt6-wayland \
        noto-fonts noto-fonts-cjk noto-fonts-emoji ttf-jetbrains-mono \
        bluez bluez-utils tlp vim git base-devel \
        intel-ucode vulkan-intel intel-media-driver libva-utils \
        sudo curl wget unzip zip screenfetch \
        xdg-desktop-portal-hyprland xdg-user-dirs xdg-utils \
        polkit lxqt-policykit gvfs gvfs-mtp \
        vulkan-tools mesa-utils thermald acpid fwupd zram-generator
```