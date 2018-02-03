### {% linkable_title Installation %}

<p class='note'>
The installation instructions assume you are running Hassbian
</p>

Example configuration:

```bash
sudo su -s /bin/bash homeassistant
cd /srv/homeassistant
source bin/activate
cd ~/.homeassistant
git clone https://github.com/maihde/hass-better-radiotherm.git
mkdir -p ~/.homeassistant/custom_components/binary_sensor
mkdir -p ~/.homeassistant/custom_components/sensor
mkdir -p ~/.homeassistant/custom_components/climate
ln -s ~/.homeassistant/hass-better-radiotherm/binary_sensor/radiotherm.py ~/.homeassistant/custom_components/binary_sensor/radiotherm.py
ln -s ~/.homeassistant/hass-better-radiotherm/sensor/radiotherm.py ~/.homeassistant/custom_components/sensor/radiotherm.py
ln -s ~/.homeassistant/hass-better-radiotherm/climate/radiotherm.py ~/.homeassistant/custom_components/climate/radiotherm.py
```

Example configuration:

```yaml
climate:
  - platform: radiotherm
    host: '192.168.1.1'
sensor:
  - platform: radiotherm
    host: '192.168.1.1'
binary_sensor:
  - platform: radiotherm
    host: '192.168.1.1'
```
