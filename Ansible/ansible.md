


## Sample Inventory File


```
#web servers

web_node1 ansible_host=web01.test.com ansible_connection=winrm ansible_user=administrator ansible_password=123
web_node2 ansible_host=web02.test.com ansible_connection=winrm ansible_user=administrator ansible_password=123
web_node3 ansible_host=web03.test.com ansible_connection=winrm ansible_user=administrator ansible_password=123

#db servers
sql_db1 ansible_host=sql01.test.com ansible_connection=ssh ansible_user=root ansible_ssh_pass=456
sql_db2 ansible_host=sql02.test.com ansible_connection=ssh ansible_user=root ansible_ssh_pass=456

#groups

[db_nodes]
sql_db1
sql_db2

[web_nodes]
web_node1
web_node2
web_node3

[mix1_nodes]
sql_db1
web_node1

[mix2_nodes]
sql_db2
web_node2
web_node3

[asia_nodes:children]
mix2_nodes
mix1_nodes
```

## Commands

 - ansible-playbook playbook-pingtest.yaml -i inventory.txt
 - 



## ansible-playbook playbook-withitems.yaml -i inventory.txt
__ansiblecontroller ansible_host=192.168.0.25 ansible_ssh_pass=123__

```
-
    name: 'List of animals'
    hosts: localhost
    vars:
        animals:
            - Rat
            - Pig
            - Badger

    tasks:
        -
            command: 'echo "{{item}}"'
            with_items: '{{animals}}'

```



__Roles__: https://galaxy.ansible.com/




https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html



MobaXterm_Portable_v22.1
https://atom.io/
apm install linter-js-yaml
http://www.yamllint.com/
apm install remote-syn
