# Ansible Role: logwatch

An ansible role to install and configure logwatch.

## Requirements

> This role has been tested on `Ubuntu 16.04` and `Ubuntu 16.10` only.

## Variables

- `logwatch_email`: email address which Logwatch reports to
  - Default: `root@localhost`
- `logwatch_detail`: the level of detail in the Logwatch report
  - Default: `low`
- `logwatch_range`: the default time range for the Logwatch report
  - Default: `yesterday`
- `logwatch_output`: the output method of the Logwatch report
  - Default: `mail`
  - Options:
    - `stdout`
    - `mail`
    - `file`
- `logwatch_format`: the format of the Logwatch report
  - Default: `text`
  - Options:
    - `text`
    - `html`
- `logwatch_daily_reports`: send daily reports
  - Default: `true`
- `logwatch_services`: list of services to monitor
  - Default: `['All']`


## Usage Example

```yaml
- hosts: all
  vars:
    logwatch_email:
      - admin@domain.tld
  roles:
    - thedumbtechguy.logwatch
```


## License

MIT / BSD

## Author Information

This role was created by [TheDumbTechGuy](https://github.com/thedumbtechguy) ( [twitter](https://twitter.com/frostymarvelous) | [blog](https://thedumbtechguy.blogspot.com) | [galaxy](https://galaxy.ansible.com/thedumbtechguy/) )

## Credits