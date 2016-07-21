# Chromeboo Setup Instructions

These are instructions are mostly for my own reference but if they are helpful
to anyone else your welcome to use them.


## Install Secure Shell
https://chrome.google.com/webstore/detail/secure-shell/pnhechapfaindjhompbnflcldabbghjo

## Install Crosh Window
https://chrome.google.com/webstore/detail/crosh-window/nhbmpbdladcchdhkemlojfjdknjadhmh

## Install Cruton
https://github.com/dnschneid/crouton

## Download Powerline Fonts
https://github.com/powerline/fonts
`ttf` and `otf` file.

## Install the Powerline Fonts
Having copied otf and ttf fonts to `~/Downloads/fonts` execute

```sh
sudo mkdir -p /usr/local/share/fonts
sudo cp ~/Downloads/fonts /usr/local/share/fonts
mkdir -p /tmp/test/
sudo mount --bind /home/chronos/ /tmp/test/
cd /tmp/test/user
cat > .fonts.conf << FONTS
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "fonts.dtd">
<fontconfig>
<dir>/usr/local/share/fonts</dir>
</fontconfig>
FONTS
exit
```
## Update Secure Shell Fonts

```
"Droid Sans Mono for Powerline","Ubuntu Mono derivative Powerline", monospace
```

## Create chroot using cruton

```
sudo sh crouton -e -n linux -r xenial -t core,cli-extra
```

