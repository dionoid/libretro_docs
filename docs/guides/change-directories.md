# Directory configuration

Next step you might want to consider is setting directories for RetroArch, this can help get the best experience possible.

Although the defaults will suit most users, if you want to configure custom BIOS's or change the save location, you will have to change directories.

Some directory variable values are set to "default" by default in retroarch.cfg. However, to modify directory values to "default", a text editor is required. "default" represents different values to different entries in `Settings` -> `Directories`:
- `<Content Directory>` -- The directory where the game was loaded from via `Main Menu -> Load Content`. For example, if /home/gamer/Downloads/SNES/game.sfc was loaded, and retroarch.cfg contains `screenshot_directory = "default"`, then the screenshots will be saved in /home/gamer/Downloads/SNES/.
- For multiple directory variables in retoarch.cfg, the "default" value sets their value in `Settings` -> `Directories` to:`<Default>` -- The RetroArch configuration directory.

Table of special values limited to some variables:

| retroarch.cfg configuration | RetroArch `Settings` -> `Directories` |
| - | - |
| system_directory = "default" | `System/BIOS`: `<Content Directory>` |
| screenshot_directory = "default" | `Screenshots`: `<Content Directory>` |

## From RetroArch:

- Open RetroArch.
- Navigate to `Settings` -> `Directories`.
- Click on the directory you want to change.
- Navigate to the desired location using the File Browser.

## From a text editor:

- Close RetroArch.
- Find your retroarch.cfg file. If you are having trouble locating the file, 1) Open RetroArch 2) Navigate to `Main Menu` -> `Configuration File` -> `Save Current Configuration`, the on-screen notification widget will display: `Saved new config to "[...]/config/retroarch/retroarch.cfg".`. If all hope is lost do a system-wide search for **retroarch.cfg**
- Open retroarch.cfg in a text editor.
- After the = sign, make changes then save the file.

# Paths to consider changing:

## Cores

This is the location for all your cores. To [install them using the user interface](download-cores.md#installing-cores-through-retroarch-interface), this setting needs to point to a writeable directory.

!!! note
    The Ubuntu PPA does not point this to a user-writable directory because cores are modified by the package manager. If you want to change it manually, you might want to change this directory from "retroarch.cfg" with a text editor since the RetroArch file browser doesn't show hidden folders by default. *libretro_directory =* is what you need to change in the config file. Some distributions use `~/.config/retroarch/cores/`

## System/BIOS

This is where you specify the location for all your BIOS's, by default RetroArch looks for BIOS in your "Starting directory" folder. It is not suggested that you dump all BIOS files in the "Starting directory".

!!! note
    Some emulators *(Example: PS1 and PSP)* will require BIOS files to even function.

It is suggested that this be changed to a folder named "system" under your retroarch config folder. If you can't be bothered to try and find this config folder (since it varies from OS), and you want to skip having to use a text editor, choose another location that the BIOS files will be.

!!! note
    You might want to change this directory from "retroarch.cfg" with a text editor since the RetroArch file browser doesn't show hidden folders by default. *system_directory =* is what you need to change in the config file.

## File Browser

Another one you'll want to consider changing. This will be the starting directory when you select "Load Content" and it can be very handy to have this set to your ROM folder. Although this probably isn't needed since RetroArch has an import feature, it doesn't hurt to have this set anyway.

## Save Files, and Save States

!!! note
    Some platforms/distros may use a different structure, so always verify your paths in settings -> directory

Last one you should consider changing are the save locations, by default it will place them in the same folder as your ROMS. If you care about organisation you should change these to another folder.
