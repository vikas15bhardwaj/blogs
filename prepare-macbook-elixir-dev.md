#### Install brew

```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"```


#### Install Spectacle (Optional good to have if you use multiple displays)

```Spectacle (https://github.com/eczarny/spectacle#keyboard-shortcuts)```

#### Install VSCode (download current version and install)

- After installing add vscode to shell path using Cmd + Shift + P -> Shell Command - Add to path```


#### Install Zshell

```sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"```

#### Install Spaceship theme for zshell

```brew install spaceship```

#### Configure Zsh 
```code ~/.zshrc```

```
autoload -U promptinit; promptinit
# Proxy Setup (if required)
export PATH=$HOME/bin:$HOME/Library/Python/3.9/bin:/usr/local/bin:$HOME/.cache/rebar3/bin:$PATH
export http_proxy=ProxyURL
export https_proxy=ProxyURL
export HTTP_PROXY=ProxyURL
export HTTPS_PROXY=ProxyURL
export no_proxy=localhost

# Enable Erlang command history in iex
export ERL_AFLAGS="-kernel shell_history enabled"

# Add plugins
plugins=(git vscode zsh_reload git-prompt)

# Add ctrl + back arrow and forward arrow

bindkey "^[^[[D" backward-word
bindkey "^[^[[C" forward-word

# Add prompt customization (date and git status)
export PROMPT='%B%F{37}%W %T %~%b$(git_super_status) % # '

```

#### Install iTerm2

#### Setup for Erlang/Elixir

- Download Xcode and Install

- brew install autoconf (Need 2.69 version)
	
```
brew uninstall autoconf --ignore-dependencies
cd
curl -O -L http://ftpmirror.gnu.org/autoconf/autoconf-2.69.tar.gz
tar -xzf autoconf-2.69.tar.gz
cdautoconf-2.69
./configure
make
sudo make install
```
- install other dependencies
```
brew install kerl
brew install wxmac
brew install unixodbc
brew install openssl
brew install coreutils
brew install gpg
brew install gawk
brew install docker-compose
brew install ansible
```
  
#### Install asdf

Recommended approach is using Git, follow steps here for Zsh
https://asdf-vm.com/guide/getting-started.html#_3-install-asdf

```	
# Clone from git
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.8.1
```

```
# Add to ~/.zshrc
. $HOME/.asdf/asdf.sh
  
```
Run ```source ~/.zshrc``` to reload terminal. You now can run asdf

#### Add plugins to install erlang, elixir, node js

```
asdf plugin add erlang
asdf plugin add elixir
asdf plugin add nodejs
npm install -g nodemon
asdf install
(not sure what this command does - something for nodejs)
bash -c '${ASDF_DATA_DIR:=$HOME/.asdf}/plugins/nodejs/bin/import-release-team-keyring'
```

#### For proxy
```
mix hex.config https_proxy ProxyURL
mix hex.config http_proxy ProxyURL
npm config setproxy ProxyURL
```

#### Install VSCode Extensions
ElixirLS

#### Issues

May need to come out of network and set no proxy to install node js to resolve error:
```
gpg: keyserver receive failed: No name
gpg: keyserver receive failed: No name
gpg: keyserver receive failed: No name
gpg: keyserver receive failed: No name
gpg: keyserver receive failed: No name
...
```

#### Download Docker

#### Download postman
