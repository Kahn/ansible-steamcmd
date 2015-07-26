steamcmd
=========

Provides a bootstrapped steamcmd install following Valves [setup guide](https://developer.valvesoftware.com/wiki/SteamCMD).

Requirements
------------

There are no pre-requisites for the steamcmd role.

Role Variables
--------------

```
# Creates a user to own the steam application.
steamcmd_user: steam
# Defines the home directory for the steamcmd_user
steamcmd_user_homedir: /home/{{ steamcmd_user }}
# Points to the steamcmd package from Valve
steamcmd_url: https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz
# Forces steamcmd to execute, defaults to true to ensure steamcmd is functional before the role exits
steamcmd_run_steamcmd: true
```

Dependencies
------------

No role dependencies.

Example Playbook
----------------

To install steamcmd on your game servers use the following playbook.

```
---
- hosts: steamcmd
  roles:
  - kahn.steamcmd
```

License
-------

GPLv3

Author Information
------------------

Sam Wilson - [http://www.cycloptivity.net/](http://www.cycloptivity.net/)
