# Vagrant w/ hyper-v

## scenario 1 - create Cent OS 
```
vagrant box add hashicop/precise64

PS C:\Users\genid> vagrant box add hashicorp/precise64
==> box: Loading metadata for box 'hashicorp/precise64'
    box: URL: https://vagrantcloud.com/hashicorp/precise64
This box can work with multiple providers! The providers that it
can work with are listed below. Please review the list and choose
the provider you will be working with.

1) hyperv
2) virtualbox
3) vmware_fusion

Enter your choice:

==> box: Adding box 'hashicorp/precise64' (v1.1.0) for provider: hyperv
    box: Downloading: https://vagrantcloud.com/hashicorp/boxes/precise64/versions/1.1.0/providers/hyperv.box
    box:
==> box: Successfully added box 'hashicorp/precise64' (v1.1.0) for 'hyperv'!

vagrant init hashicorp/precise64

A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.

vagrant up --provider hyperv
PS C:\Users\genid\vagrant-works\lab1-test> vagrant up --provider hyperv
Bringing machine 'default' up with 'hyperv' provider...
==> default: Verifying Hyper-V is enabled...
==> default: Verifying Hyper-V is accessible...
==> default: Importing a Hyper-V instance
    default: Creating and registering the VM...
    default: Successfully imported VM
    default: Please choose a switch to attach to your Hyper-V instance.
    default: If none of these are appropriate, please open the Hyper-V manager
    default: to create a new virtual switch.
    default:
    default: 1) l2-internal
    default: 2) External
    default: 3) Internal
    default: 4) External-wired
    default: 5) Default Switch
    default:
    default: What switch would you like to use? 1
    default: Configuring the VM...
    default: Setting VM Enhanced session transport type to disabled/default (VMBus)
==> default: Starting the machine...
==> default: Waiting for the machine to report its IP address...
    default: Timeout: 120 seconds
Hyper-V failed to determine your machine's IP address within the
configured timeout. Please verify the machine properly booted and
the network works. To do this, open the Hyper-V manager, find your
virtual machine, and connect to it.

The most common cause for this error is that the running virtual
machine doesn't have the latest Hyper-V integration drivers. Please
research for your operating system how to install these in order
for the VM to properly communicate its IP address to Hyper-V.
PS C:\Users\genid\vagrant-works\lab1-test>


# login 
vagrant cloud auth login

# vm destroy
PS C:\Users\genid\vagrant-works\lab1-test> vagrant destroy
    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Stopping the machine...
==> default: Deleting the machine...

```
