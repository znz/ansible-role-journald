# Ansible role for `journald`

- Create `/var/log/journal`
- Add `journald_users` to `systemd-journal` group

## Requirements

- Debian
- Ubuntu

## Role Variables

### Common

- `journald_users`: users

## Dependencies

None.

## Example Playbook

Normal usage:

    ---
    - hosts: all
      become: yes
      roles:
      - znz.journald

With users:

    ---
    - hosts: all
      become: yes
      roles:
      - { role: znz.journald, journald_users: ['foo', 'bar'] }

## License

MIT License
