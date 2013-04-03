IndigoHue Plugin for Perceptive Automation Indigo
==================================================

## Summary
This plugin extends Indigo allowing it to communicate with the Philips Hue Lighting System.

## Installation
* Download this zip file: https://github.com/alistairg/IndigoHue/zipball/master
* Unzip the file. A folder will be created.
* With Indigo running, double-click the file "Hue.indigoPlugin" inside the folder created above
* Follow the Indigo dialog and enable the plugin.
* The plugin should now be visible in the Plugins drop-down as "Hue Lighting Control".

## Configuration
### Bridge Setup
* Go into "Hue Lighting Control" on your Plugin menu, choose "Configure..."
* Enter the IP Address of your bridge. You may find this via the iPhone/iPad app (not Android) or via the www.meethue.com website once you have registered your bridge.
* Click OK to close the plugin settings
* Press the center button on your hue hub
* Open the settings again (yes, this could be easier.... I'll fix it this weekend!) and press the "Retry Pairing" button
* You should see a message in the Event Log that pairing succeeded.
* Select Plugins -> Hue Lighting Control -> Reload to retrieve a fresh list of devices.

### Adding Bulbs
* Add a new device to Indigo.
* Choose Type: Hue Lighting Control
* Choose Model: Hue Bulb (only choice)
* Pick the Hue bulb from the list (this is downloaded from Hue, and will match the names you've set there)
** If you don't see any bulbs listed, make sure you performed the last step in the bridge setup above.
* Save

## Controlling Lights
* Indigo's standard On, Off, Dim controls will work
* To set a colour, create an action and choose Plugin | Hue Lighting Control | Set Color as your action
* Pick the bulb to control
* Fill in RGB values with a scale of 0-255 for each
* Run the action to change the color