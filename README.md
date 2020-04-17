Knot
=========
Manage Knot DNS Authoritative master & slave Servers

Requirements
------------

Debian 9
Debian 10

Role Variables
--------------

A description of the settable variables for this role :

server: "127.0.0.1"
zone1: "{{ vault_zone1 }}"
zone2: "{{ vault_zone2 }}"
domain1: "{{ vault_domain1 }}"
domain2: "{{ vault_domain2 }}"
subdomain: "test"

update: "del"
TTL: "3600"
champs: "TXT"
value: "Ansible text block test"

ssh_admin_pubkey: "{{ vault_ssh_admin_pubkey }}"
admin_mail: "{{ vault_admin_mail }}"
dns_key: "{{ vault_dns_key }}"
key_update_local: "{{ vault_key_update_local }}"

slave:
  ip: "{{ vault_slave.ip }}"
  ip6: "{{ vault_slave.ip6 }}"
  fqdn:  "{{ vault_slave.fqdn }}"

master:
  ip: "{{ vault_master.ip }}"
  ip6: "{{ vault_master.ip6 }}"
  fqdn: "{{ vault_master.fqdn }}"

hypervisor:
  ip: "{{ vault_hypervisor.ip }}"
  ip6: "{{ vault_hypervisor.ip6 }}"

spam:
  ip: "{{ vault_spam.ip }}"
  hostname: "{{ vault_spam.hostname }}"

stor:
  ip: "{{ vault_stor.ip }}"
  hostname: "{{ vault_stor.hostname }}"

nas:
  ip: "{{ vault_nas.ip }}"
  hostname: "{{ vault_nas.hostname }}"

mail:
  ip: "{{ vault_mail.ip }}"
  hostname: "{{ vault_mail.hostname }}"

webmail:
  ip: "{{ vault_webmail.ip }}"
  hostname: "{{ vault_webmail.hostname }}"

hme:
  ip: "{{ vault_hme.ip }}"
  ip6: "{{ vault_hme.ip6 }}"
  hostname: "{{ vault_hme.hostname }}"

dkim_values: "{{ vault_dkim_values }}"

app:
  ip: "{{ vault_app.ip }}"

cloud:
  ip: "{{ vault_cloud.ip }}"
  hostname: "{{ vault_cloud.hostname }}"

dkim2_values: "{{ vault_dkim2_values }}"

tlsa_domain2: "{{ vault_tlsa_domain2 }}"

tlsa_domain1: "{{ vault_tlsa_domain1 }}"

Dependencies
------------

no dependencies

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

Matthieu FONTANA <matthieu.fontana@itcloud.ovh>
