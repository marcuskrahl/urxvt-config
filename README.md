# urxvt-config

This repository contains config files to be used with urxvt (rxvt-unicode). 
It uses Perl plugins from [muennich/urxvt-perls](https://github.com/muennich/urxvt-perls muennich/urxvt-perls)

## Install urxvt

On Arch Linux run:

  sudo pacman -S rxvwt-unicode xsel ttf-dejavu
  
## Install the config file

Clone the repository:
  
  git clone https://github.com/marcuskrahl/urxvt-config
  
Replace the .XResources file:

  mv ~/.XResources ~/.XResources.original
  ln -s urxvt-config/XResources ~/.XResources
  
To use the Perl plugins for selection, URL selection and copy paste, copy the following files:

  cp urxvt-config/plugins/* ~/.urxvt/ext/
  
## Usage

Make sure to apply the changes:

  xrdb -load ~/.XResources
  
The configuration should load automatically on login in most cases. If the configuration is not loaded add the following command to your .xinitrc:

  [[ -f ~/.Xresources ]] && xrdb -merge ~/.Xresources
  
When the changes are applied you can run urxvt by its command and you should immediately see the new configuration in action
