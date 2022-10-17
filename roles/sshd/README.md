Role Name
=========

This role installs and configures the sshd system daemon.

Requirements
------------

This role checks for the existence of required python selinux packages if running on an SELinux enabled target. Verify that these are installed prior to running the role.

Role Variables
--------------

Most configuration variables are named similarly to the sshd_config directives they template. Be sure to always quote any "yes" or "no" directives due to yaml otherwise interpreting these as booleans which will fail to template.
Freeform blocks can be added prior to other config to override later config with _sshd\_freeform\_overrides_, or added as Match directives at the end via _sshd\_match\_blocks_.

Additional Notes
----------------

Max startups has been raised slightly by default under the assumption that this host will be accessed via Ansible frequently, to prevent lockouts.

License
-------

BSD

