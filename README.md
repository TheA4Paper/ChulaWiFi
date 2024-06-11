# ChulaWiFi
How to connect to ChulaWiFi with NetworkManager
## Preface
Many of you may wonder why do we even need a guide to connect to chula WiFi, well, that's because I have been struggling to connect to WPA2-Enterprise network for the past 3 days until I randomly stumble upon a solution and I don't want any other Linux users to suffer the same fate as myself.
I haven't tried to recreate the problem with any other configurations other than ArchLinux+Gnome+NetworkManager yet so I am not sure what exactly is the problem.
When I tried to connect to ChulaWiFi via the provided GUI, it just straight up did nothing after I click "connect". Heck, it didn't even remember the credentials.
## Solution
You can try edit the config file yourself but I wouldn't be talking about that here as people may have different setup that require different configuration files and that if you want to, you should already know how to do it without a guide.
### Install nm-connection-editor
  Try running the editor to see if it's install on your system
  ```
  nm-connection-editor
  ```
  If you're using ubuntu, NetworkManager + the editor should be preinstalled, if not
  ```
  sudo apt install network-manager
  ```
  Other distros
  ```
  sudo pacman -S nm-connection-editor #Arch
  ```
### Add a new network
Once you launch your nm-connection-editor with commandline or as an app called "Advanced Network Configuration" you will see a list of all your configured network. You will need to add ChulaWiFi or if it already exists, delete it with "-" button.
<img src="https://github.com/TheA4Paper/ChulaWiFi/assets/80894853/556b66aa-66c3-4935-95d8-7c0c396f7ce2" width="400" />

Once clicked "+" button, you will be prompted to select a connection type. Select "Wi-Fi"
<img src="https://github.com/TheA4Paper/ChulaWiFi/assets/80894853/c13f2905-de40-4de8-b7ef-7a00542e3fff" width="400" />

After word, you will be shown a menu not too dissimilar to the standard gnome wifi setting. Name your network, this can be whatever but I will go with "ChulaWiFi" and add the SSID for your network, in this case "ChulaWiFi"

<img src="https://github.com/TheA4Paper/ChulaWiFi/assets/80894853/531a6ab7-f1ca-4644-98dc-eb22238c6738" width="400" />

Finally, move on the the "Wi-Fi Security tab. Configure exactly as shown in the picture **except for username as passoword** use the one for your CUNET instead and click save.

<img src="https://github.com/TheA4Paper/ChulaWiFi/assets/80894853/d315aa75-99c5-496c-b702-6157d1938f9c" width="400" />

Now, you should be able to connect to your wifi via the built-in wifi settings as usual.

<img src="https://github.com/TheA4Paper/ChulaWiFi/assets/80894853/7eadd839-7016-4a66-bd27-65f3c0cb49c4" width="400" />
