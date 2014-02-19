nova_snapshot
=============

ansible module for nova snapshoting

example:
- name: Snapshot instance
  nova_snapshot:
       auth_url: "{{ os_auth_url }}"
       login_username: "{{ os_username }}"
       login_password: "{{ os_password }}"
       login_tenant_name: "{{ os_tenant_name }}"
       instance_name: "{{ item.name }}"
       snapshot_name: snapshot1
  with_items: nodes

