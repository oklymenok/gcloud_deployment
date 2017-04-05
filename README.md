Dependencies
------------

* gcloud is installed and configured

What does it do ?
------------

* Creates network / subnet
* Creates 2 firewall rules to allow SSH and ICMP
* Creates instance template
* Creates InstanceGroupManager with 10 Instances
* Runs bash script on every machine and creates /root/test.file

Usage
------------

run me:


```
gcloud deployment-manager deployments create first-deployment --config main.yaml 
```

FAQ
------------

* Modify startup-script:
  vim nstance_templates/compute.jinja
* Modify firewall rules
  vim network/public_net.jinja
* Increase/Decrease instances number
  vim main.yaml
  change TARGET_SIZE to the desired value
