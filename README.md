# Vino Manager

## or just "vino"

> from the Italian word "vino", literally "wine"

A Bash dmenu based script for managing wine prefixes and quickly launch apps

## Requirements

- bash
- dmenu
- wine
- winetricks

## Install and use

Just download the `vino` file (or clone the repo),
copy it in your `PATH` and run it.

It will open a menu where you can create, configure,
delete prefixes and run an already configured app.

Create a new prefix and give it a name,
vino will run `winecfg` to let you configure stuff,
when you close wine config a new menu appears;
This will let you chose an action inside the prefix:
Winecfg, Winetricks, Run EXE and Create Runner;
the first two launch the respective command inside the prefix,
"Run EXE" will let you run an exe or msi file inside the prefix
(useful to run installer programs),
"Create Runner" will ask you for a main exe file and then
create a `run.sh` script that will be used to quickly launch your installed app.

Once a runner has been generated,
an App can be launched directly using the `run.sh` file
inside the prefix folder (`~/vino/[prefix name]/run.sh`);
or you can use the "Launch app" option on the main menu.

Prefixes are all saved inside `~/vino/` each folder is the prefix name given during configuration.

## TODO

I would like to add more features in the future,
like Wine-GE versions management, DXVK and VKD3D install
