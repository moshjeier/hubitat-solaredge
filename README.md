# hubitat-solaredge
Hubitat driver to query the Solaredge API for inverter metrics and site overview.

# Installation
1. Copy contents of [solaredge-driver.groovy](https://github.com/funzie19/hubitat-solaredge/blob/master/solaredge-driver.groovy) into your Hubitat `Drivers Code` section.
1. Under the `Devices` section, create a new virtual device by clicking `Add Virtual Device`.
    1. Enter a `Device Name`.
    1. Select the `Solaredge Monitoring Driver`.
    1. Save the device.
    1. The device is now installed and ready to be configured.
    
# Configuration
Setting | Required | Default | Description
------------ | ------------- | ------------- | -------------
Site Id | Yes | Empty | Site Id for location being monitored.
API Key | Yes | Empty | This key is either provided by the installer, or generated by the user if they have access granted to them by the installer or have the inverter under their own installed account.
Solaredge Monitoring API URL | Yes | `https://monitoringapi.solaredge.com` | Solaredge monitoring API url, this can change in the future or used by any other developer for their testing purposes.
How often to refresh the energy data | Yes | Non Selected | Select how often to refresh energy data. Remember the Solaredge API allows a max of 300 calls per day.
How often to refresh the production overview data | Yes | Non Selected | Select how often to refresh the production overview data. Remember the Solaredge API allows a max of 300 calls per day.
How often to refresh power flow data | Yes | Non Selected | Select how often to power flow energy data. Remember the Solaredge API allows a max of 300 calls per day.
Daily Energy Details Title | No | Empty | Title for `Energy Details` tile, if left blank title will not display.
Production Overview Title | No | Empty | Title for `Production Overview` tile, if left blank title will not display.
Power Flow Title | No | Empty | Title for `Power Flow` tile, if left blank title will not display.
Display last updated timestamp? | No | False | Option to display last updated timestamp on tiles.
Enable debug logging | No | False | Enable debugging of logs.

# Dashboard
To add to dashboard select the device name created. Pick `Attribute` as the template. Then either select `energy_tile` or `overview_tile` to display the summary tiles. Otherwise select individual attributes.

### Example:

![Tile Example](/tiles.png)
