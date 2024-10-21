# Ansible Role: Puppet

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

An Ansible Role that installs [Puppet](https://www.docker.com) on Linux.

## Requirements

Requires Java 7 or later to be installed on the server (you can use the `nholuong.java` role to install Java if needed; see the test playbook in `tests/` for an example).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    puppet_package: puppetserver

The package to be installed.

    puppet_service: puppetserver
    puppet_service_state: started
    puppet_service_enabled: false
    puppet_service_manage: false

The service that should be run on this server. By default, this role will not manage a Puppet service, and will not enable it at boot time.

    puppet_bin_path: /opt/puppetlabs/bin

The path to all the Puppet Labs binaries (after the package is installed).

    # Used only for Debian/Ubuntu.
    puppet_apt_deb: "https://apt.puppetlabs.com/puppet6-release-{{ ansible_distribution_release }}.deb"

The .deb file for installation on Debian-based OSes.

    # Used only for RedHat/CentOS.
    puppet_yum_rpm: "https://yum.puppet.com/puppet6-release-el-{{ ansible_distribution_major_version }}.noarch.rpm"

The .rpm file for installation on RedHat-based OSes.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - nholuong.puppet

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟