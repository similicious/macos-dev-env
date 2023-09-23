# MacOS dev environment

## Installation

  1. Ensure Apple's command line tools are installed (`` to launch the installer).
  2. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html):

     1. Run the following command to add Python 3 to your $PATH: `export PATH="$HOME/Library/Python/3.9/bin:/opt/homebrew/bin:$PATH"`
     2. Upgrade Pip: `sudo pip3 install --upgrade pip`
     3. Install Ansible: `pip3 install ansible`

## Run playbook

```
# Install requirements
ansible-galaxy install -r requirements.yml

# Run playbook
ansible-playbook main.yml -K

# Run playbook, only tagged
ansible-playbook main.yml -K --tags "defaults"
```