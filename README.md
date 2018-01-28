# dotfiles
Robert's Configuration dotfiles

## Table of Contents:
1. [ZSH Terminal Setup](#zsh-iterm-config)
2. [Atom configuration](#atom-configuration)

# ZSH iTerm Config

## tl;dr
- Editor: [Sublime](https://www.sublimetext.com/)
- ZSH: [Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
    - Theme: [https://github.com/bhilburn/powerlevel9k](https://github.com/bhilburn/powerlevel9k)
- Terminal: [iTerm](https://www.iterm2.com/)
    - Theme: [Solarized Dark theme](https://github.com/altercation/solarized)
    - Font: [Source Code Pro Powerline Patched](https://github.com/powerline/fonts)

## iTerm2

    brew cask install iterm2
    
Recommended Theme

- [Solarized Dark theme](https://raw.githubusercontent.com/mbadolato/iTerm2-Color-Schemes/master/schemes/Solarized%20Dark%20-%20Patched.itermcolors) (patched version to fix the bright black value)

## Oh My Zsh 

URL: https://github.com/robbyrussell/oh-my-zsh

Install:
    
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
 
## Powerlevel9k

    git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k

Update `~/.zshrc` with `ZSH_THEME="powerlevel9k/powerlevel9k"`.

My `~/.zshrc` inlcudes my preferred Powerlevel prompt styling. See other options [here](https://github.com/bhilburn/powerlevel9k/wiki/Stylizing-Your-Prompt)

Additionally, see what other users are doing [here](https://github.com/bhilburn/powerlevel9k/wiki/Show-Off-Your-Config).

## Patched Font

Download and install a [patched Powerline font](https://github.com/powerline/fonts) or download the patched source code pro font in the fonts directory.

Set the font in iTerm (iTerm → Preferences → Profiles → Text → Change Font → Source Code Pro); restart iTerm.

## Sublime Configuration

**1. Create a directory at ~/bin**

```mkdir ~/bin```

**2. Copy sublime to the newly created ~/bin directory**

```ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" ~/bin/subl```

**3. Add the following to your `~/.zshrc` file**

```export PATH=$PATH:$HOME/bin```

>NOTE: My included `.zshrc` already includes this

**4. Set sublime as your default editor in your `~/.zshrc` file**

```    
export EDITOR='subl'
export VISUAL='subl'
```

>NOTE: My included `.zshrc` already includes this

**5. Restart terminal and test the sublime command**

```subl ~/.zshrc```

If your .zshrc file opens in Sublime you are good to go! 

Source and additional resources for Sublime setup can be found here: https://gist.github.com/barnes7td/3804534

# Atom Configuration

View [my package list](https://github.com/Rmafive/dotfiles/blob/master/atom/atom-packages.txt) or generate your own package list:

     apm list --installed --bare > package-list.txt

Import my list using: 

    apm install --packages-file ./package-list.txt


