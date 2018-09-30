ansible-role-import-gpg-repo
============================

[![GitHub license](https://img.shields.io/github/license/bluk/ansible-role-import-gpg-repo.svg)](https://github.com/bluk/ansible-role-import-gpg-repo/blob/master/LICENSE) [![Build Status](https://travis-ci.org/bluk/ansible-role-import-gpg-repo.svg?branch=master)](https://travis-ci.org/bluk/ansible-role-import-gpg-repo)

An [Ansible](https://www.ansible.com) role to clone a repository and import public [GPG](https://www.gnupg.org/) keys from it.

Requirements
------------

It is assumed GPG is already installed and is available on the `$PATH`.

Role Variables
--------------

* `git_repo` - The git URL to clone.

* `git_repo_local_dest` - The path to clone the files to.

* `git_repo_dir_src` - The path in the git repository to import GPG keys from.

* `git_accept_hostkey` - If the hostkey should automatically be accepted.

* `git_force` - If the repository should discord changes in the directory.

* `git_recursive` - If any submodules should be checked out.

* `git_remote` - The name of the remote to give.

* `git_update` - If the repository should be updated.

* `git_verify_commit` - If the commit's GPG signature should be verified.

* `git_version` - The version to checkout.

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: bluk.import_gpg_repo }
```

License
-------

Apache 2.0
