# Ansible Role PostgreSQL Databases

Library of Ansible plugins and roles for deploying various services.
See [ansible-roles](https://github.com/davidfischer-ch/ansible-roles) for additional documentation.

This repository hosts the role PostgreSQL Databases and may depend of other roles and plugins of the library.

## Dependencies

This role has no requirements.

## Variables

TODO VARIABLES

## Example

### PlayBook

```
- hosts:
    - database
  roles:
    - postgresql-databases
  vars:
    postgresql_databases_role_action: setup
```

### Variables

```
postgresql_databases:
  template1:
    name: template1
    extensions: []
  application:
    template: template1
    extensions: []
    name: my-database
    users:
      - name: my-user
        password: some-password-here
        role_flags: [SUPERUSER, CREATEDB]
        clients:
          - all  # see https://stackoverflow.com/questions/3278379/how-to-configure-postgresql-to-accept-all-incoming-connections
```

## License

See [LICENSE.rst](LICENSE.rst).

## Authors

See [AUTHORS](AUTHORS).

2014-2022 - David Fischer
