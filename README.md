
ansible-role-wireguard
======================


Linux
-----

This role should work with:

- Ubuntu 20.04 (Focal Fossa)

host.ini example
----

```
[wg]
wg   ansible_host=fqdn_or_ip
```

Playbook example
----
```
- name: Install VPN | wireguard
  hosts: wg
  roles:
    - ansible-wireguard
  vars:
    wireguard_peers:
      phone:
        friendly_name: phone
        Address: "10.9.0.10/32"
        PublicKey: UJlLYeqNfzgz3rGwN1nEtOuAlBErsVvATCKpYdZYpXg=
      tablet:
        friendly_name: tablet
        Address: "10.9.0.11/32"
        PublicKey: hs3r+PiWu8Mxnc1yo7BlaWnnHM3Ggwe90Km7U5M2qj8=
```

