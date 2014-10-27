# sshcd

Tired of having to type this janky command to [ssh](http://manpages.ubuntu.com/manpages/saucy/en/man1/ssh.1.html) and [cd](http://manpages.ubuntu.com/manpages/saucy/en/man1/cd.1posix.html) into unfamiliar remote servers?

```sh
ssh -t user@fraction.io "cd /foo/bar; exec \$SHELL"
```

Stop it. Connect with SSH and cd (change directory) with one command.

```sh
sshcd user@fraction.io:/foo/bar
```

## Installation

Use Homebrew to download and install the executable.

```sh
brew tap fraction/homebrew-formulae
brew install sshcd
```

Alternatively, download the executable into your path with a single command.

```sh
sudo curl -o /usr/local/bin/sshcd https://raw.githubusercontent.com/fraction/sshcd/master/sshcd
```

## Usage

The default usage is pretty simple.

```sh
sshcd user@fraction.io:/foo/bar
```

The tool supports prepended flags, too!

```sh
sshcd -v user@fraction.io:/foo/bar
```
