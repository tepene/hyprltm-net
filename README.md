# 🌐 HyprLTM-Net

A high-performance network management interface for **Hyprland**, powered by **Rofi** and **NetworkManager (nmcli)**. 

Easily scan, connect, and manage your Wi-Fi, Ethernet, and VPN connections from a sleek Rofi menu, designed for speed and simplicity.

https://github.com/user-attachments/assets/7da1d5b8-d8a1-47f4-8809-e82efc078ab2


## ✨ Features

- **Interactive Security:** Secure prompts for password entry with hidden characters and a toggle to show/hide the key.
- **LTMNight Themed:** Inherits system colors via the `ltmnight.rasi` palette.
- **Comprehensive Controls:**
    - **Wi-Fi:** Scan for nearby networks, connect to new ones, or manage existing SSIDs.
    - **Wired:** Quickly switch between different Ethernet profiles and configurations.
    - **VPN:** Modular support for **Wireguard** and **OpenVPN**, including the ability to import profile files directly through the interface.
    - **Status:** View real-time connection details, local/public IP addresses, and DNS info.
- **Connection Management:** Dedicated menu to **Edit Passwords**, **Rename** connections, or **Forget/Delete** old profiles.
- **Lightweight & Fast:** Zero background process overhead—runs only when triggered.


## 🛠 Prerequisites

Ensure the following are installed on your system:

| Package | Purpose |
| :--- | :--- |
| `networkmanager` | Backend connection management (`nmcli`) |
| `rofi-wayland` | The graphical menu engine |
| `Nerd Fonts` | Required for icons (e.g., *JetBrainsMono Nerd Font*) |
| `libnotify` | (Optional) For desktop notifications |


## 🚀 Installation & Usage

### 1. Clone the Repository
```bash
git clone https://github.com/hyprltm/hyprltm-net.git
cd hyprltm-net
```

### 2. Move Configuration Files
```bash
mkdir -p ~/scripts && mv hyprltm-net.sh ~/scripts/ && chmod +x ~/scripts/hyprltm-net.sh
mkdir -p ~/.config/rofi/themes/ && cp *.rasi ~/.config/rofi/themes/
```
### 3. Setup Keybind or Waybar Click
Choose your preferred way to launch the menu:

Via Keyboard Shortcut: Open ~/.config/hypr/hyprland.conf and add this line:
```bash
bind = SUPER, N, exec, ~/scripts/hyprltm-net.sh
```
Via Waybar: Open ~/.config/waybar/config.jsonc and add the on-click action to your network module:
```bash
"network": {
    "on-click": "~/scripts/hyprltm-net.sh"
}
```
## 🎨 Theming

`HyprLTM-Net` uses the **LTMNight** color palette. To customize the appearance, edit `~/.config/rofi/themes/ltmnight.rasi`.

| Variable | Description | Default |
| --- | --- | --- |
| `@ltmnight9` | Primary Accent | Purple (#bd93f9) |
| `@ltmnight0` | Background | Dark Gray (#282a36) |
| `@selection` | Selection Highlight | Semi-transparent Gray |



## ☕ Support the Project

If you find this tool helpful and want to support its development and the **HyprLTM** ecosystem, consider supporting me through the following platforms:

[![Buy Me A Coffee](https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=☕&slug=linuxtechmore&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff)](https://www.buymeacoffee.com/linuxtechmore)


Every bit of support helps keep the project alive and ensures I can spend more time developing open source tools for the Linux community!


## 📄 License

**Created by [Djalel Oukid (sniper1720)](https://github.com/sniper1720)** and distributed under the **GPL-3.0 License**. See [LICENSE](https://github.com/hyprltm/hyprltm-net/blob/main/LICENSE) for more information.

*Check out more Linux & Open Source content on my [website!](https://www.linuxtechmore.com)*
