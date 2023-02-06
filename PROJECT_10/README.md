# ANSIBLE FOR COMPLETE STACK SETUP (V PROFILE)

##  Pre-Requisite
+   AWS account
+   Ansible
+   IDE (Sublime, Vscode)
+   Github account, Git 

##  The following setup must be done after the provision of [VPC](https://github.com/sadebare/AWS_DEVOPS_PROJECTS/tree/main/PROJECT_9)
##  FIRST PHASE SETUP SYSTEM DESIGN
![system_design](./images/provision_instances.png)
### During this phase, we will be using ansible playbook to configure multiple ec2 for our vprofile application setup and load balancer

+ First we will be merging the bastion variable to the vpc setup variable
+ Create a new file called [site.yml](./site.yml) with the following content

      ---
      - import_playbook: vpc-setup.yml
      - import_playbook: bastion-instance.yml
+ Launch an EC2 instance to install ansible and fetch the code


## SECOND PHASE SETUP SYSTEM DESIGN
![system_design_2](./images/setup2.png)
### Finally, we get to setup our playbook to setup our vprofile stack
