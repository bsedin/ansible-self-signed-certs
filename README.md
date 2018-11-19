# ansible-self-signed-certs
Ansible role to manage self signed certificates

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-self-signed-certs.git library/self-signed-certs
```

Use role:

```yaml
---
- hosts: cdn01.yourserver.io
  remote_user: ansible
  become: true
  roles:
    - self-signed-certs
```

See default variables at `defaults/main.yml`.
