Ansible for Zabbix
===========
Ansible playbook for setup to Zabbix Server.

## Spec
- CentOS 7
- Ansible 2.3 or newer
- Apache 2.4
- MariaDB 5.5
- PHP 5.6

## Prepared
Edit to the target host.
`vagrant`
```
[zabbix-server]
localhost ansible_connection=local
```

Create to credentials on MariaDB.
`vars/private.yml`
```yaml
mariadb_root_password: "your mysql root password"
mariadb_default_user_password: "your zabbix user password"
```

## Run
```bash
ansible-playbook setup.yml
```
