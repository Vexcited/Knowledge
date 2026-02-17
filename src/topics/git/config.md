# Config

Here's all the global configuration I use across all my projects.

```sh
git config --global gpg.format ssh
git config --global gpg.ssh.program ssh-keygen
git config --global gpg.ssh.allowedSignersFile .gitsigners

git config --global tag.gpgSign true
git config --global commit.gpgsign true

git config --global rerere.enabled true
git config --global fetch.pruneTags true
git config --global core.ignorecase false
```

## User Configuration

```sh
git config --global user.name "Your NAME"
git config --global user.email "your@email.com"
```

Finally, here I like to add a global `signingkey` that I use almost everywhere but I try to prevent this lately.
Per project, I do the following.

```sh
git config user.signingkey "ssh-ed25519 MY_PUBLIC_KEY"
```

The adequate private key will be pulled by Bitwarden's SSH agent since I self-host Vaultwarden.
