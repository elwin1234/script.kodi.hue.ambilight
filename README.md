#script.kodi.hue.ambilight

A Kodi add-on that controls Philips Hue lights. 

##Light Groups

This add-on works with a concept of groups that are different from groups defined on Hue bridge. Each group can have 0 or more lights and has default behavior settings that can be modified in the add-on settings screen. After playback ends, the add-on will try to restore the lights to where they where before it started controlling them.

###Theater Group

Lights in the theater group act like wall lights in a typical theater. When playback starts the lights dim and they undim when playback is paused or ends. If you only want some of the lights to undim during pause, it is possible to configure "subgroup" in `add-on settings -> Theater` and only dim the subgroup.

###Ambilight Group

Ambilight group tries to control the lights similarly to modern ambilight TVs. The add-on tries to figure out the most represented colors in each frame and change the lights to reflect that. They can also be configured to work similarly to theater group when playback is paused.

### Static Group

Static lights act opposite to the theater lights -- they are turned on when playback starts, turned off when you pause the playback and go back to initial state after the playback stops.

##Installation

The add-on requires Kodi add-on "requests".

**Kodi add-on script.module.requests**

 - download the add-on as a ZIP file from https://github.com/beenje/script.module.requests
  - (click on the green "Clone or download button" then click on the "Download ZIP" link)
 - open Kodi
 - go to `Add-ons -> click on the opened box in top left corner -> Install from zip file -> navigate to the downloaded zip file`
 - select the zip file.

**Kodi add-on script.kodi.hue.ambilight**

 - download the add-on as a ZIP file from the top of this page
  - (click on the green "Clone or download button" then click on the "Download ZIP" link)
 - go to `Add-ons -> click on the opened box in top left corner -> Install from zip file -> navigate to the downloaded zip file`
 -  restart Kodi and configure the add-on:
   - `Add-ons -> My add-ons -> Services -> Kodi Philips Hue -> Configure`
   - click `Discover Hue Bridge` and follow the instructions (press button on the Hue bridge)
   - setup the groups and tweak settings to your liking

##Support
If you find a problem or missing feature, open an issue or a pull requests on https://github.com/mpolednik/script.kodi.hue.ambilight.

To have a higher chance of issue being solved, please attach a log file. To record one, go to `settings wheel -> System settings -> Logging -> Enable Debug Logging` and follow the procedure at http://kodi.wiki/view/Log_file/Easy

##Note for Raspberry Pi users:
 - Save the add-on configuration by exiting Kodi before shutting down the Pi completely
 - Ambilight mode doesn't work on a Raspberry Pi due to the way it renders video
