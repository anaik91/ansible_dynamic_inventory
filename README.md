# ansible_dynamic_inventory

## Pre Reading

Please read the following background material on [Dynamic Inventory](https://www.jeffgeerling.com/blog/creating-custom-dynamic-inventories-ansible).

## Test invnetory 

```
$ ./inventory.py 
{"_meta": {"hostvars": {}}}

$ ./inventory.py  --list
{"group": {"hosts": ["127.0.0.1"], "vars": {"ansible_connection": "local"}}, "_meta": {"hostvars": {"127.0.0.1": {"host_specific_var": "foo"}}}}

```


## Test as below

```
./test.sh 
127.0.0.1 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}

```