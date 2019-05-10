# Comply with update subnet API


## Demo steps
Execute the following steps:

```bash
git clone https://github.com/oVirt/ovirt-provider-ovn

# check the version that is *not* complying with the networking API
git checkout 1.2.21

# launch the integration test environment
automation/create_it_env.sh

# execute the playbook
ansible-playbook -i localhost demo_bugfix_1707739.yml
```

As can be seen, the playbook execution didn't fail, but, the subnet was not
updated.

To showcase the change, follow the steps below:

```bash
git checkout 1.2.22

# remove all the docker containers in the integration test environment
docker rm -f $(docker ps -q -f "label=purpose=ovirt_provider_ovn_integ_tests")

# relaunch the integration test environment
automation/create_it_env.sh

# execute the playbook
ansible-playbook -i localhost demo_bugfix_1707739.yml
```

## Customize the demo
As per the openstacksdk [configuration guide](https://docs.openstack.org/openstacksdk/rocky/user/connection.html), by updating the [clouds.yml](clouds.yml)
file, you can connect to another ovirt-provider-ovn instance.

