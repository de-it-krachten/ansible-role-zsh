[![CI](https://github.com/de-it-krachten/ansible-role-zsh/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-zsh/actions?query=workflow%3ACI)


# ansible-role-zsh

Installs zsh w/ my-zsh



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- Red Hat Enterprise Linux 10<sup>1</sup>
- RockyLinux 8
- RockyLinux 9
- RockyLinux 10
- OracleLinux 8
- OracleLinux 9
- OracleLinux 10
- AlmaLinux 8
- AlmaLinux 9
- AlmaLinux 10
- SUSE Linux Enterprise 15<sup>1</sup>
- openSUSE Leap 15
- Debian 11 (Bullseye)
- Debian 12 (Bookworm)
- Debian 13 (Trixie)
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS
- Fedora 41
- Fedora 42

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# List of packages
zsh_packages:
  - zsh

# Instals ohmyzsh
zsh_ohmyzsh: true

# Zsh theme for ohmyzsh
zsh_theme: agnoster

# ZSH additions
zsh_zshrc: |
  # personal additions
  source ~/.zshrc.add
  # direnv
  eval "$(direnv hook zsh)"
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'zsh'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'zsh'
      ansible.builtin.include_role:
        name: zsh
</pre></code>
