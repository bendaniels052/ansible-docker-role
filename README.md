## Ansible Role: Docker CE 'Community Edition'

Ansible Role to install [Docker CE](https://docs.docker.com/engine/installation/linux/docker-ce/centos/)
It will automatically configure the storage with direct-lvm which is recommended for Production

This role will only install the latest community editon of docker.
If you require this role to support other versions, then please contact [G IT&S CBAF Automation Engineering](mailto:gitscbafautomationengineering@bp.com)

## Requirements

Optional, for direct-lvm mode, make sure the deevice /dev/xvdcz is present

## Role Variables

None.

## Dependencies

None.

## Variables

``` docker_additonal_volume```: OPTIONAL - default is set to true. However if you dont need docker installed on a differen LV then set the varible to false. When set to true, you will be able to use the `Docker Storage Size` varibales.


## Example Playbook

```yaml
- hosts: my_hosts
  roles:
    - { name: docker, docker_additonal_volume: false }
```


