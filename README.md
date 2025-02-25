# TeamCity build agent installation

This ansible role installing and configure simple teamcity build agent

## Requirements

The target host for running the Teamcit build agent must be configured in advance:
  - Java virtual machine installed;
  - connection to the network port of the Teamcity build agent is available.

## Dependencies

None

## Options

The adress (uri) of your TeamCity server
```
teamcity_server_url: https://localhost
```

Account, that you cat specify at this variable, must to be configured on the target in advance.
```
teamcity_build_username: "{{ teamcity-agent | default(ansible_user) }}"
```

## Example Playbook

```
- hosts: teamcity-agent
  vars:
    teamcity_server_url: http://teamcity.some.tld
    teamcity_build_username: builder
  roles:
    - spr0sto.teamcity-agent

```

# Author Information

# License

