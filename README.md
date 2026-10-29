# tst

An Ansible role that installs Apache and deploys an `index.html` page.

## What it does

- Installs the `apache2` package
- Copies `files/index.html` to `/var/www/html/index.html`

## Requirements

- Ubuntu or Debian target machines
- Ansible 2.12 or newer
- A user with sudo rights (`become: true`)

## Example playbook

```yaml
---
- hosts: test
  become: true
  roles:
    - tst
```

## Usage

```
ansible-playbook -i inventory.ini first.yaml
```

## Notes

Apache uses port 80. Do not run this role on machines that already run
nginx on port 80.

## License

MIT

## Author

Nour2603
