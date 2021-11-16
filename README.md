# homeassistant-paxcalima
Home assistant Custom component for  Pax Calima fan

This is offered AS IS. Feel free to fork. 
Developed and tested in HA version 2021.11.04 

## Installation: 

1. Put __init__.py, sensor.py, manifest.json into <config>/custom_components/paxcalima/ on your home assistant installation (where <config> is the directory where your config file resides).
2. Restart Home Assistant.
3. Add following to your configuration.yaml:

```yaml
sensor:
  - platform: paxcalima
    mac: 00:11:22:AA:BB:CC # replace with MAC of your Pax Calima (see below if not known).
    pin: 57854677 # Replace with you pin code (found from devices motor unit)
    name: Projector Room(optional)
```
4. Check configuration
5. Restart Home Assistant

## Find out PAX MAC address (if not known):
 
### Option 1 install from pypi:

 1. Install calima
 ```
python3 -m pip install calima
 ```
 
 2. Scan for devices
 ```
 calima -l
 ```
 
 3. Take note of the MAC address. 
 
 
 ### Option 2 install from github repo:

 1. Download pycalima
```
#Get latest pycalima on to your work directory 
wget https://github.com/PatrickE94/pycalima/archive/master.zip
unzip master.zip
cd pycalima-master
```
 
2. Run cmdline.py 
```
python3 cmdline.py -l
```

3. Take note of the MAC address. 

