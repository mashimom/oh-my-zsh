# oh-my-zsh

Ansible role to install and configure oh-my-zsh on both APT and YUM based distros.
> Tested on Ubuntu 14.04 64bit and Fedora 21 64bit.

## Role Variables

The role's variables are:

| Variable | Default value | Description |
|----------|---------------|-------------|
| `ohmyzsh_plugins` | `[git, vagrant, docker, command-not-found, gradle, lein]` | List of the plugins that should be added to oh-my-zsh. |
| `ohmyzsh_theme` | `pygmalion` | Theme to be set on oh-my-zsh. |
| `ohmyzsh_disable_auto_update` | `"true"` | Disable oh-my-zsh auto update. |
| `ohmyzsh_users_home_base_dir` | `/home` | Base directory for users homes.  If defined, all users who have homes in this directory will have oh-my-zsh enabled. Override with `!!null` if not required. |
| `ohmyzsh_root_home` | `/root` | If defined, oh-my-zsh will be installed for root in this directory. Override with `!!null` if not required. |

## Example Playbook

Including an example of how to use this role:

    - hosts: all
      roles:
         - { role: mashimom.oh-my-zsh, ohmyzsh_theme: "lambda" }

## License

[Apache License v2.0](LICENSE)
