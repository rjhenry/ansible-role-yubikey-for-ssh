# Ansible Role: Yubikey for SSH

An Ansible Role that installs and configures tools such that a system can use GPG keys located on a [Yubikey](https://yubico.com) for SSH access. It also conveniently sets up the same key for GPG use.

## Requirements

There are no requirements on the managed machine, though note that this is
designed to be run locally. As such, you may need the ansible tools installed on
the machine in question.

## Role Variables

There are two *required* variables for this role: `gpg_key_url` and
`gpg_key_fingerprint`.

`gpg_key_url` must be a URL that your GPG key can be fetched from; for example,
`https://gpg.rickhenry.uk/rjh@rick-h.xyz.asc`.

`gpg_key_fingerprint` is the fingerprint of that key, with no spaces between the
sections. This allows the key to be set as trusted.
TODO: Use this to verify the downloaded GPG key.

## Dependencies

None.
