
# Track 1: Configure ACI using Terraform

## Module 1: Install and Setup Terraform

In this lab, the focus will be on using Terraform as a way to provide operational rigor to your network device configurations. You will first learn how to install and use Terraform on Cisco network solutions, like ACI.

Terraform is distributed as a binary for almost all platforms (Windows, Linux, Mac). You can use various methods of installing and they are all explained in detail on the [Terraform](https://www.terraform.io/) website in the file [download location](https://www.terraform.io/downloads.html).

Step 1: For this lab we are going to download Terraform from the website and install it on this CentOS machine directly. This is to ensure that this lab has tested with this specific version of Terraform. Execute the following commands.

```
[root@centos7-tools1 ~] # cd ~
[root@centos7-tools1 ~] #  wget https://releases.hashicorp.com/terraform/1.3.2/terraform_1.3.2_linux_amd64.zip
```

Step 2: Unzip the Terraform package.

```
[root@centos7-tools1 ~] #  unzip terraform_1.3.2_linux_amd64.zip
```

Step 3: View the inventory to see the terraform binary was created. 

```
[root@centos7-tools1 ~] # ls
```

Step 4: Move the terraform binary to /usr/local/bin/


```
root@centos7-tools1 ~] # mv terraform /usr/local/bin/
```

![](imgs_1/terraform_install.png)

### Verify the Terraform Installation

Step 1: Enter terraform -help to make sure terraform installed and it displays the available commands for execution


```
root@centos7-tools1 ~] # terraform -help 
```

```
$ terraform -help
Usage: terraform [global options] <subcommand> [args]

The available commands for execution are listed below.
The primary workflow commands are given first, followed by
less common or more advanced commands.

Main commands:
  init          Prepare your working directory for other commands
  validate      Check whether the configuration is valid
  plan          Show changes required by the current configuration
```

Step 2: terraform -version will show the terraform version that we installed.

```
$ terraform -version
Terraform v1.3.2
on linux_amd64
```

The following are some of the terraform commands that will be useful when doing the lab.

**Terraform Init:** Is the initial command that the user will run under the Configuration files to initialize the working directory. This command will check the configuration files and download the necessary provider plugins.

**Terraform Plan:** This command allows the user to create an execution plan. This command is very useful because allows the user to check and compare if the execution plan matches the desired intent of the plan.

**Terraform Apply:** This is the command that applies the changes to execute the desired state of the configuration.

**Terraform Destroy:** This is the command that allows the user to "destroy" (delete) the Terraform managed infrastructure

### **Proceed to [Module 2](https://github.com/krishna426426/ACI_Infrastructure_as_Code/blob/main/module2.md)**
