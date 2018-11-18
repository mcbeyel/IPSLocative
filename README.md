# IPSLocative

This is an IP-Symcon plugin for receiving POST notifications sent by the free app "Locative" (http://get.locative.io/) 


## Installation

* Install Locative for free from the Apple Appstore
* Create a new Geofence in the app
* Choose your home location
* Give your home a unique ID. In IP-Symcon a variable with the same name will be created, containing the absence status
* Use `http://_your IP-Symcon IP_:_your IP-Symcon port_/hook/locative?name=_a_name_for_your_home` for both URLs
Example: `http://1.2.3.4:3777/hook/locative?name=Zuhause`

Unfortunately, the Locative App does not forward the name of your geofence automatically, so you have to add it as a parameter to the URL.
* Enable HTTP Basic Authentication and enter username and password
* In IP-Symcon add the "Locative" module and enter the same username and password
* After the first message has been recorded, you will see additional variables automatically created as child items of the Locative module

## Testing

* Open the settings dialog in the Locative app
* Set "Global HTTP settings" to `http://_your IP-Symcon IP_:_your IP-Symcon port_/hook/locative?name=_a_name_for_your_home&status=1`
* The `status=1` will simulate presence, `status=0` will simulate absence
