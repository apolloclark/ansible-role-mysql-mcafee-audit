# Ansible Role: mysql-mcafee-audit

Ansible Role to install and configure McAfee Audit plugin. https://github.com/mcafee/mysql-audit

## Requirements

MySQL server.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

https://github.com/mcafee/mysql-audit/wiki/Configuration

Version of the plugin to install.

	mcafee_plugin_version: "1.1.4-725"

Location of the configuration directory.

	mysql_config_include_dir: "/etc/mysql/conf.d"

Location of the audit log file.

	audit_json_log_file: "/var/log/mysql/audit.log"

Enable the JSON log file.

	audit_json_file: "ON"

Force logging: Connect, Quit and Failed Login commands, regardless of the settings in audit_record_cmds and audit_record_objs variables.

	audit_force_record_logins: "ON"

mysqld binary checksum validation

	audit_validate_checksum: "OFF"

## Dependencies

Must have installed MySQL Server. I would suggest:

    apolloclark.mysql

## Example Playbook

    - hosts: all
      roles:
        - apolloclark.mysql-mcafee-audit

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Apollo Clark](https://www.apolloclark.com/)
