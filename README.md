# Install-GITLAB-on-RHEL-8

## Update your system and install the required dependencies:

```bash
sudo yum -y update
```
```bash
sudo yum -y install curl vim policycoreutils python3-policycoreutils
```
## If you want to install and use local mail server for sending notifications, then install Postfix:
```bash
sudo yum -y install postfix
```
## Start and enable Postfix service after the installation.

```bash
sudo systemctl enable postfix && sudo systemctl start postfix
```
## Add the Gitlab CE Repository
```bash
curl -s https://packages.gitlab.com/install/repositories/gitlab/gitlab-ce/script.rpm.sh | sudo bash
```
## Install GitLab CE on CentOS 8 / RHEL 8
```bash
sudo yum install gitlab-ce
```
## Configure GitLab CE on CentOS 8 / RHEL 8
```bash
vim /etc/gitlab/gitlab.rb
```

```bash
external_url 'http://gitlab.example.com'
```

```bash
sudo gitlab-ctl reconfigure
```
