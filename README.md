# Openshift UPI installation on hetzner with ansible

manage quay with ansible operator in openshift

## Prerequisites

```pip3 install ansible hcloud```


## Create server 

```ansible-playbook playbooks/create_server.yml -i auth/hcoud.yml```

## Create bastion 

```ansible-playbook playbooks/bastion.yml -i auth/hcoud.yml```

## Activate rescue

```ansible-playbook playbooks/activate-rescue.yml -i auth/hcoud.yml```

## Install rhcos and ignition file

```ansible-playbook playbooks/install_rhcos.yml -i auth/hcoud.yml```

## Restart server

```ansible-playbook playbooks/restart_server.yml -i auth/hcoud.yml```

## Configure identity provider 

```ansible-playbook playbooks/configure-idp.yml -i auth/hcoud.yml```











