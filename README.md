# Host notes

This repository is a host's configuration and state. `./hostctl` is its admin interface
(`./hostctl help`). Configuration lives in `etc/`, state in `state/`, logs in `var/log/`.

- ntp may use only the servers in `etc/ntp.allowed.json`.
- metrics needs `max_open_files` of at least 1024 (vendor guidance).
- Backups go to a mounted volume (`state/mounts.json` lists the mounts).
- smartd skips its self-test except on Sundays; the "self-test skipped" line is normal.
- The printer service is disabled on purpose by the owner.
