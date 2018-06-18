# my-osx-settings
My OSX Settings

### brew
```
https://brew.sh
brew cask
brew tap caskroom/versions

brew cask install alfred

brew cask install jetbrains-toolbox
brew cask install sublime-text
brew cask install sourcetree
brew cask install iterm2

brew cask install docker

brew cask install 1password
brew cask install authy

brew cask install dropbox
brew cask install slack

brew cask install google-chrome
brew cask install postman
brew cask install appcleaner

brew install awscli
brew install aws-elasticbeanstalk
brew install awslogs

brew install wget
brew install httpstat

brew install jenv
brew install scalaenv

brew install rbenv
brew install ruby-build

brew install nodenv
brew install node-build

brew install pyenv
brew install pyenv-virtualenv
brew install autoenv
```

### App Store
```
Line
KakaoTalk

Airmail 3
Reeder 3

Status Clock
Weather Wall
```

### Menually
```
Dynamon
```

### .bash_profile
```
PS1="\u@\h \w $ "

export TERM=xterm-color
export CLICOLOR=1
export LSCOLORS=ExFxCxDxBxegedabagacad
export GREP_OPTIONS='--color=auto'
export GOPATH=/usr/local/go
export HISTTIMEFORMAT="%y/%m/%d %T "

alias ls='ls -GFh'
alias ll='ls -l'
alias la='ls -la'

function ssh-aws-ec2user() { ssh -i ~/.ssh/xxx.pem ec2-user@"$1"; }
alias as=ssh-aws-ec2user

function git-pull-all() {
    START=$(git symbolic-ref --short -q HEAD);
    for branch in $(git branch | sed 's/^.//'); do
        git checkout $branch;
        git pull ${1:-origin} $branch || break;
    done;
    git checkout $START;
};

function git-push-all() {
    git push --all ${1:-origin};
};

# Env Series
eval "$(jenv init -)"
eval "$(rbenv init -)"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
source $(brew --prefix autoenv)/activate.sh
eval "$(scalaenv init -)"
eval "$(nodenv init -)"
```

### Setting

##### .bash_profile
```
ln -s ~/Dropbox/Mac/bash_profile ~/.bash_profile
```

##### Use ⌥ ← and ⌥→ to jump forwards/backwards words in iTerm 2, on OS X
`Profiles > Keys`
```
Keyboard Shortcut: ⌥←
Action: Send Escape Sequence
Esc+: b

Keyboard Shortcut: ⌥→
Action: Send Escape Sequence
Esc+: f
```

##### Show access modifier for classes in IntelliJ
`Command + Shift + A` > `Registry`
```
-Dide.projectView.show.visibility=true
```

##### Convert '₩' to '\`'
```
curl -sSL https://gist.githubusercontent.com/redism/43bc51cab62269fa97a220a7bb5e1103/raw/0d55b37b60e0e0bd3d0d7f53995de0a722f9820c/kr_won_to_backquote.sh | sh
```
