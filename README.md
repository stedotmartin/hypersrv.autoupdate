# Ansible Role: hypersrv.autoupdate

This role will configure Ubuntu or RHEL to automatically install updates

Tested only on

- Ubuntu 16.04
- CentOS 7.4

## Requirements


## Role Variables

    autoupdate_mail

Email to send notifications to.

    autoupdate_non_security

Set to true to update all packages not just security updates

    autoupdate_reboot

Set to true to auto reboot server if needed at 3am

     autoupdate_mail_only_on_error

Ubuntu only, Only send notifications if there is an error with auto updating.

## Dependencies

None.

## Example Playbook

      - hosts: all
        become: true
        vars:
            autoupdate_mail: "alerts@somedomain.com"
            autoupdate_non_security: true
            autoupdate_reboot: true
            autoupdate_mail_only_on_error: false
        roles:
            - role: hypersrv.autoupdate

## License

MIT

## Author Information

Stephen Martin <sm at hypersrv(dot)com>