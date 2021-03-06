# i3config
My configuration file(s) and scripts for the i3-wm.

**MASTER** - _Hopefully stable branch._\
**DEV** - _Development Branch (latest changes)_

## WHAT IS IT?

If you're an i3-wm (i3 Window Manager) user like me, you'll probably be interested in checking out other people's configuration files, or maybe even trying their setups like a theme. Well, you're more than welcome to do so with mine, that's why it's on GitHub! That, and it's easier for me to manage.

## WHAT'S ON OFFER?

* Tidy, carefully-written `config` and addons.
* Useful shell script for further initializing.
* Function library (`.libi3bview`) with over 40 outputs.
* Optional twin bars with extensive statistics, via libi3bview.
* Optional transparency for i3bar. (`i3bar_trans`)
* The `partmount` addon for quick, easy filesystem mounting.
* Repository updates for the foreseeable future.
* Various special XF86 keys already set.
* No endless busy cursor -- correct exec calls.
* Shortcuts for taking various screenshot types.
* Shortcut for a webcam window at the touch of a button(s).
* No indicator, for the more experienced users.
* Standard i3-wm (touch-type) mapping scheme.
* No need to mess around with modes.
* Various keyboard shortcuts for MOC.
* Sink and source volume support, using PulseAudio.
* Wallpaper slideshow using feh. (`feh_slides`)
* Many `for_window` corrections already set.
* Shortcut to toggle keyboard autorepeat.

...and probably other things I'm missing.

## REQUIREMENTS & SUGGESTIONS

To get the most out of this setup, or to even have it working at all like it does for me, you'll need the following Ubuntu and/or Debian based packages, and their dependencies:

```
alsa-utils - Utilities for configuring and using ALSA
compton - compositor for X11, based on xcompmgr
dunst - dmenu-ish notification-daemon
feh - imlib2 based image viewer
fonts-opensymbol - OpenSymbol TrueType font
i3-wm - improved dynamic tiling window manager
i3blocks - highly flexible status line for the i3 window manager
i3lock - improved screen locker
libnotify-bin - sends desktop notifications to a notification daemon (Utilities)
moc - ncurses based console audio player
pulseaudio-utils - Command line tools for the PulseAudio sound server
scrot - command line screen capture utility
suckless-tools - simple commands for minimalistic window managers
x11-apps - X applications
xfce4-terminal - Xfce terminal emulator
xorg - X.Org X Window System
```

You may also want to try my compton.conf settings file. Install with insit:

```bash
insit -C miscellaneous compton.conf $HOME/.config/compton.conf 644 $UID $UID
```

If you use MOC, you might find mplay useful. Install with insit:

```bash
sudo insit -C miscellaneous mplay /usr/bin/mplay 755 0 0
```

If you use dunst, I have a feeling you'll enjoy my settings. Install with insit:

```bash
insit -C miscellaneous dunstrc $HOME/.config/dunst/dunstrc 644 $UID $UID
```

## INSTALLATION

Visit the installit repository to use the easy-to-use TFL downloader.

## USING COMPTON

Although compton isn't required for this setup, I strongly recommend it, as i3-wm is a bit lackluster without it. If you decide to use compton, check out my compton.conf settings and, if you like, copy them over to `$HOME/.config/compton.conf`, but be sure you check it for anything which wouldn't be compatible with your setup or especially hardware.

I use an nVidia GPU and a 64-bit Intel CPU, if that helps at all.

## MAKING CHANGES

If you'd like to make changes to the configuration files, this section might help you, particularly if you're not familiar with i3-wm.

#### Selecting Own PulseAudio Devices

As mentioned above my i3-wm setup has a few event sounds. I used to have a lot, but they honestly got annoying after a while. I've since found a happy medium between sounds and silence, using discreet sounds when it's most useful to have audible feedback, mostly to ensure I actually pressed the key properly!

If you see "paplay" (might help to search for it with your text editor), then there's a good chance it's pointing to either a variable assigned to a filename, or the filename itself. This is what you want to change. Using paplay does however limit you to certain file types; for example, paplay will not play mp3 files, or at least it doesn't for me. Your best bet is to use ogg or wav, or look online to see which file formats it supports out of the box.

## ...to be continued!
