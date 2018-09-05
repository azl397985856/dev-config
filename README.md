# dev-config

开发过程中一系列工具的配置

## zsh

```
# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH=/Users/luxiaopeng/.oh-my-zsh

# Set name of the theme to load. Optionally, if you set this to "random"
# it'll load a random theme each time that oh-my-zsh is loaded.
# See https://github.com/robbyrussell/oh-my-zsh/wiki/Themes
ZSH_THEME="robbyrussell"
# Set list of themes to load
# Setting this variable when ZSH_THEME=random
# cause zsh load theme from this variable instead of
# looking in ~/.oh-my-zsh/themes/
# An empty array have no effect
ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

# Uncomment the following line to use case-sensitive completion.
# CASE_SENSITIVE="true"

# Uncomment the following line to use hyphen-insensitive completion. Case
# sensitive completion must be off. _ and - will be interchangeable.
# HYPHEN_INSENSITIVE="true"

# Uncomment the following line to disable bi-weekly auto-update checks.
# DISABLE_AUTO_UPDATE="true"

# Uncomment the following line to change how often to auto-update (in days).
# export UPDATE_ZSH_DAYS=13

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to disable auto-setting terminal title.
# DISABLE_AUTO_TITLE="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
# COMPLETION_WAITING_DOTS="true"

# Uncomment the following line if you want to disable marking untracked files
# under VCS as dirty. This makes repository status check for large repositories
# much, much faster.
# DISABLE_UNTRACKED_FILES_DIRTY="true"

# Uncomment the following line if you want to change the command execution time
# stamp shown in the history command output.
# The optional three formats: "mm/dd/yyyy"|"dd.mm.yyyy"|"yyyy-mm-dd"
# HIST_STAMPS="mm/dd/yyyy"

# Would you like to use another custom folder than $ZSH/custom?
# ZSH_CUSTOM=/path/to/new-custom-folder

# Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(
  git
  git-flow
)

source $ZSH/oh-my-zsh.sh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# ssh
# export SSH_KEY_PATH="~/.ssh/rsa_id"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"
alias cls='clear'
alias nis='cnpm i --save'
alias myip='curl http://ipecho.net/plain'
alias s="sudo"

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion

export PATH="$HOME/.yarn/bin:$PATH"

# Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$PATH:$HOME/.rvm/bin"

# tabtab source for electron-forge package
# uninstall by removing these lines or running `tabtab uninstall electron-forge`
[[ -f /Users/luxiaopeng/.nvm/versions/node/v8.9.3/lib/node_modules/electron-forge/node_modules/.2.2.2@tabtab/.completions/electron-forge.zsh ]] && . /Users/luxiaopeng/.nvm/versions/node/v8.9.3/lib/node_modules/electron-forge/node_modules/.2.2.2@tabtab/.completions/electron-forge.zsh
source /Users/luxiaopeng/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

## VSCODE

### setting

gistID：7a78ffb25f4c82f0269552c49fc3f0fb

使用 setting syn，输入上面的 gistId 即可下载对应配置

配置同步地址： https://gist.github.com/azl397985856/7a78ffb25f4c82f0269552c49fc3f0fb

### extensions

```bash
➜  ~/.vscode/extensions
➜  extensions ls
KnisterPeter.vscode-commitizen-0.5.0
Shan.code-settings-sync-2.9.0
christian-kohler.npm-intellisense-1.3.0
christian-kohler.path-intellisense-1.4.2
dbaeumer.vscode-eslint-1.4.8
esbenp.prettier-vscode-1.2.2
jcbuisson.vue-0.1.5
msjsdiag.debugger-for-chrome-4.3.0
octref.vetur-0.11.7
shinnn.stylelint-0.33.3
waderyan.gitblame-2.4.1
```

## WTF-util

```yml
wtf:
  colors:
    background: black
    border:
      focusable: darkslateblue
      focused: orange
      normal: white
  term: "xterm-256color"
  grid:
    columns: [35, 35, 35, 35, 35, 35]
    rows: [10, 10, 10, 10, 10, 3, 4]
  refreshInterval: 1
  mods:
    git:
      commitCount: 5
      commitFormat: "[forestgreen]%h [grey]%cd [white]%s [grey]%an[white]"
      dateFormat: "%H:%M %d %b %y"
      enabled: true
      position:
        top: 0
        left: 2
        height: 2
        width: 2
      refreshInterval: 8
      repositories:
        - "/Users/luxiaopeng/duiba-h5-sign/"
        - "/Users/luxiaopeng/duiba-h5-activity/"
    todo:
      checkedIcon: "X"
      colors:
        checked: gray
        highlight:
          fore: "black"
          back: "orange"
      enabled: true
      filename: "todo.yml"
      position:
        top: 0
        left: 0
        height: 1
        width: 1
      refreshInterval: 3600
    ipinfo:
      colors:
        name: blue
        value: white
      enabled: true
      position:
        top: 0
        left: 1
        height: 1
        width: 1
      refreshInterval: 150
    gitlab:
      enabled: true
      position:
        top: 1
        left: 0
        height: 2
        width: 2
      refreshInterval: 300
      domain: "http://gitlab2.dui88.com"
      projects:
        duiba-h5-activity: "frontend"
      username: "lucifer"
    system:
      enabled: true
      position:
        top: 2
        left: 2
        height: 1
        width: 2
      refreshInterval: 3600
```

## Iterm

[配置文件](https://github.com/azl397985856/dev-config/blob/master/iTerm/com.googlecode.iterm2.plist)

## Charles

[配置文件](https://github.com/azl397985856/dev-config/blob/master/charles/)

## Dash

[配置文件](https://github.com/azl397985856/dev-config/blob/master/dash/Dash.dashsync)

## 未完待续
