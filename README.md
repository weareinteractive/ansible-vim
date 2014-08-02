# Ansible Vim Role

[![Build Status](https://travis-ci.org/weareinteractive/ansible-role-vim.png?branch=master)](https://travis-ci.org/weareinteractive/ansible-role-vim)
[![Stories in Ready](https://badge.waffle.io/weareinteractive/ansible-role-vim.svg?label=ready&title=Ready)](http://waffle.io/weareinteractive/ansible-role-vim)

> `vim` is an [Ansible](http://www.ansible.com) role which: 
> 
> * installs vim 
> * configures vim

## Installation

Using `ansible-galaxy`:

```
$ ansible-galaxy install franklinkim.vim
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):

```
$ arm install franklinkim.vim
```

Using `git`:

```
$ git clone https://github.com/weareinteractive/ansible-role-vim.git
```

## Variables

```
# vim_config:
#   - "set tabstop=2"
#   - "set shiftwidth=2"
#   - "syntax enable"

# global vim configuration
vim_config: []
```

## Example playbook

```
- host: all
  roles: 
    - franklinkim.vim
  vars:
    vim_config:
      - 'set tabstop=2'
      - 'set shiftwidth=2'
      - 'syntax enable'
```

## Testing

```
$ git clone https://github.com/weareinteractive/ansible-role-vim.git
$ cd ansible-role-vim
$ vagrant up
```

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License
Copyright (c) We Are Interactive under the MIT license.
