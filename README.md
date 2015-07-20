# Diskcheck Server
====

This repo is build, provision Diskcheck server using fabric,ansible.
All processiongs are started from fabric. So Ansible is implemented in fabric.

## Usage

### Command to create disk check server.
```
fab -l 124.24.58.33 diskcheck.build_vm
```

### Command to add disk for diskcheck server.
```
fab -l 124.24.58.33 diskcheck.add_disk
```
### Command to delete mounted disk for diskcheck server.
```
fab -l 124.24.58.33 diskcheck.delete_disk
```
### Command to check mounted disk for diskcheck server.
```
fab -l 124.24.58.33 diskcheck.check_disk<
```

## Todo
- [ ] ZABBIX のバージョン指定ができていない
- [ ] 仮想マシンデプロイ部分ができていない

### Deploy diskcheck vm
- clone vm
- set ip address

#### Common setup
- change repo
- yum update
- add repo
- install development tools

#### Zabbix agent setup
- add Zabbix repo
- install zabbix agent

#### Diskcheck tools setup
- install ioping
- install dstat
- install dbench

