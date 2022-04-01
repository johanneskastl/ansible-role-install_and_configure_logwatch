install_and_configure_logwatch
=========

Install and configure Logwatch

Requirements
------------

None.

Role Variables
--------------

Apart from installing logwatch you can set some options, if you wish. All of the role variables below are undefined by default.

All undefined options will be omitted from the file and the default value from e.g. `/usr/share/logwatch/default.conf/logwatch.conf` will be used.

- `logwatch_output`: whether logwatch should output to `stdout`, a `file` or to a `mail` (logwatch default: `stdout`)
- `logwatch_filename`: file to save the report to, only useful in combination with `Output: file`) (logwatch default: no default value)
- `logwatch_format`: output format, can be `text` or `html` (logwatch default: `text`)
- `logwatch_mailto`: mail recipient (logwatch default: `root`)
- `logwatch_mailfrom`: mail sender (logwatch default: `Logwatch`)
- `logwatch_range`: date range to use (logwatch default: `Yesterday`)
- `logwatch_detail`: level of detail for the report (logwatch default: `Low`)
- `logwatch_mailer`: which mailer to use (logwatch default: `/usr/sbin/sendmail -t`)
- `logwatch_service`: the services to report on (logwatch default: `All`)
- `logwatch_tmpdir`: temp directory (logwatch default: `/var/cache/logwatch`)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: 'johanneskastl.install_and_configure_logwatch' }

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
