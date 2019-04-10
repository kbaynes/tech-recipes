
# Install NVM n Ubuntu on Windows Subsystem for Linux

Followed [this guide](https://www.liquidweb.com/kb/how-to-install-nvm-node-version-manager-for-node-js-on-ubuntu-12-04-lts/) to install NVM

Note:
- Be sure to check for the latest version of npm at the [Creatonix GitHub](https://raw.githubusercontent.com/creationix/) and update the install nvm cURL command with the newest version.
-  Be sure to check the versions of node with nvm ls-remote, and choose the LTS (Long Term Support) latest versions.

```
sudo su
apt-get update
\#install nvm
curl https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash
\# close and reopen terminal to start using nvm
exit
exit
\# Reopen Ubuntu WSL, no need to sudo to root this time
\# Confirm NVM working
nvm -v
nvm ls-remote
nvm install 8.15.1
```

# Note on errors

The following commands:
- npm -v
- npx -v
- node -v

Will return the following obscure error on WSL if not installed:
```
this._handle.open(options.fd);
Error: EINVAL: invalid argument, uv_pipe_open
```

The solution, of course, is to simply install the packages.
