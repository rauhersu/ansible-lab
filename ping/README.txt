Prerequisite:

Set your client public ssh key in the server authorized keys, to make Ansible
commands passwordless:

$ ssh-copy-id rauherna@192.168.122.113

Next, ping the server:

$ ansible all -i hosts -m ping
192.168.122.113 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
