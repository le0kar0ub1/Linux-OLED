# Linux-OLED

OLED linux screen control.

Firstly, here is the bible https://wiki.archlinux.org/index.php/backlight.

This repository contain a script wrapper for the `gammastep` (`redshift` fork).

# Install

Install the package `gammastep` (AUR-available for archlinux).

Install the content of `Linux-OLED/etc` in `usr/local/etc/` and `Linux-OLED/bin` in `usr/local/bin`.
You can also modify the path in the script.

# Config

The `etc` directory contain static and dynamic config that you should modify for your personnal usage.

*OLED_BACKLIGHT_CORRECTION_BACKLIGHT* = the current backlight
*OLED_BACKLIGHT_CORRECTION_STEP* = inc/dec the backlight by this number
*OLED_BACKLIGHT_CORRECTION_GPS* = latitude:longitude
*OLED_BACKLIGHT_CORRECTION_BACKLIGHT_MAX* = maximum backlight
*OLED_BACKLIGHT_CORRECTION_BACKLIGHT_MIN* = minimum backlight

# Usage

`gammastep-wrapper (+|-|=(0|[1-9][0-9]?|100))`

`+` increase *OLED_BACKLIGHT_CORRECTION_BACKLIGHT* by *OLED_BACKLIGHT_CORRECTION_STEP* and apply to the screen.

`-` decrease *OLED_BACKLIGHT_CORRECTION_BACKLIGHT* by *OLED_BACKLIGHT_CORRECTION_STEP* and apply to the screen.

`=$PERCENT` set backlight to $PERCENT and apply to the screen. $PERCENT must be between the maximum and minimum defined in the config.

You *must* wait 5 seconds between screen modification because of `gammastep`.

# Epilogue

Feel free to fork, use, improve.