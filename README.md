Ansible Role: AWSCLI
=========

This role to manage awscli users.

Requirements
------------

None.

Role Variables
--------------

```
awscli_users: 
  # Add the user 'johnd'
  - name: johnd
    state: present
    configure:
      - profile: default
        aws_access_key_id: XXXXXXXXXXXXXXXXXXXX
        aws_secret_access_key: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
        output: json
        region: ap-northeast-1
  # Remove the user 'johnd'
  - name: johnd
    state: absent
 ```

Dependencies
------------

None.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: kotarella1110.awscli }
```

License
-------

MIT

Author Information
------------------

This role was created in 2016 by Kotaro Sugawara.
