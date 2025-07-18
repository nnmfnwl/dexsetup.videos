### Steps needed to produce video tutorial for `dexsetup.installer`
  * Have `server` `Debian GNU/Linux with Mate-desktop` installed, but it could be same machine as well.
```
https://www.debian.org/
```
  * Have `server` with `dconf-editor` package installed.
```
apt -y install dconf-editor
```
  * Reset `server` user's dconf environment options to make GUI look same.
```
dconf reset -f /org/mate/
```
  * Have `client` machine with `vokoscreenNG` installed.
```
apt -y install vokoscreen-ng
```
  * make `server` accessible by SSH by installing openssh server
```
apt -y install openssh-server
```
  * On `client` open Terminal tab 1 with ssh connection to `server` and clear after to be used at time of recording video
```
ssh user3@10.10.10.10..
clear
```
  * On `server` remove or backup `~/dexsetup` and `~/.bitcoin` `~/.litecoin` ... they could stay for reinstall or update cases
  * On `client` open Terminal tab 2 with ssh tunnel to `server` and clear after to be used at time of recording video
```
ssh -L 5923:127.0.0.1:5903 10.10.10.10.. -N
clear
```
  * On `client` open Terminal tab 3 with VNC connection over tunnel to `server` and clear after to be used at time of recording video
```  
remmina -c vnc://127.0.0.1:5923
clear
```
  * On `client` open web browser tab 1 with page
```
https://blocknet.org/
```
  * On `client` open web browser tab 2 with page
```
https://github.com/nnmfnwl/dexsetup/tree/merge.2025.02.06#list-of-dexsetup-components
```
  * On `client` open web browser tab 3 with page
```
https://github.com/nnmfnwl/dexsetup/tree/merge.2025.02.06
```
  * On `client` open web browser tab 4 with page
```
https://github.com/nnmfnwl/dexsetup.cli.installer
```
  * On `client` open `vokoscreenNG` and configure
    * tab 1 select full screen
    * tab 2 build in audio check
    * tab 3 frames 18, format webm, videocodec vp8, quality 9
    * Enable showclick, Enable Halo
  * On `client` voice synthesizer page to generate audio from audio.01.txt
```
https://google.com
```
  * Take care to start audio few seconds after video recording because, it suppose to not record audio correctly
  * As voice will never be at sync with video at time of recording, we split text into multiple files to be used as stop at the end of sequence and playlist play next when voice needed again for example in VLC player which can be configured to stop after every media played in playlist.
