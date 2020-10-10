Install and configure remoteIoT client
=========

Basic installation and configuration role for remoteIoT client.


Requirements
------------
- Root access
- RemoteIot account (Register [here](https://remoteiot.com/portal/?link=signup))
- Generated setup key ([See](#setup-key-generation))


Setup Key Generation
--------------
1. Log in to your remoteIoT account ([here](https://remoteiot.com/portal/?link=login)).
2. Click on your avatar in the upper left corner and select option "Assignment Token".
3. The token you'll see is your personal setup key.


Role Variables
--------------
Required:  
- setup_key - individually generated key ([See](#setup-key-generation))
- setup_name - device's name for the RemoteIoT website

Optional:  
- setup_note - additional information about a device for the RemoteIoT website
- setup_group - device's group for the RemoteIoT website
- reduce_usage (default: false) -
- schedule_upgrade (default: false) -


Example Playbooks
----------------
Minimalistic:  
```
    - hosts: 192.168.0.50
      roles:
         - { role: ansible-remoteiot-client, setup_key: example@gmail.com, setup_name: wdvaddjjkdloqpcz }
```
With all options being used:  
```
    - hosts: 192.168.0.50
      roles:
         - { role: ansible-remoteiot-client, setup_key: 9JJWAS5A6789VHAS4PQD000314J8W743, setup_name: Sensor01 , setup_note: "Enviro Station - Living Room", setup_group: Sensors, reduce_usage: true, schedule_upgrade: true }
```


License
-------

MIT
