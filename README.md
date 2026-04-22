# Codex Hero Course Homepage

This is the public repository [Be a Codex Prototyping Hero (for PMs/Designers)
](https://maven.com/p/9857db/be-a-codex-prototyping-hero-for-p-ms-designers) Maven course.

## GitHub Pages

GitHub Pages deploys automatically from `.github/workflows/deploy-pages.yml`.
It publishes the repository root `index.html` as the site.

Before starting the class, please follow the steps below to get your computer set up.

## Before You Start

- This setup assumes you are on `macOS`.  Message me through Mavven if you have a different OS.
- You will use the `Terminal` app for the command-line steps.
- Install the items in the order shown below.

## Part 1: Download And Install Apps

These apps are point-and-click installs from their web pages.

### Required downloads

1. Install Xcode  (macOS only)
   https://apps.apple.com/us/app/xcode/id497799835?mt=12

2. Install Git  
   https://git-scm.com/

3. Install VS Code  
   https://code.visualstudio.com/

4. Install Codex Desktop  
   https://openai.com/codex/

5. Install Homebrew  
   https://brew.sh/

6. Install Apple Container (macOS only)
   https://github.com/apple/container/releases/download/0.11.0/container-0.11.0-installer-signed.pkg

#### Optional for-fun-only downloads

1. Install Ghostty  
   https://ghostty.org/

2. Install Oh My Zsh  
   https://ohmyz.sh/

## Part 2: Run Commands In Terminal

Open the `Terminal` app and run these commands one step at a time.

### 1. Install `fnm`

`fnm` is a Node.js version manager. You can use `nvm` instead, but this guide uses `fnm`.

Read more: https://github.com/Schniz/fnm

Install it with Homebrew:

```bash
brew install fnm
```

### 2. Make `fnm` start automatically in Terminal

Run:

```bash
touch ~/.zshrc && { grep -Fq 'eval "$(fnm env --use-on-cd --shell zsh)"' ~/.zshrc || printf '\n# Added by fnm\neval "$(fnm env --use-on-cd --shell zsh)"\n' >> ~/.zshrc; }
```

Then open a new Terminal window, close current one.

### 3. Install Node.js

Run:

```bash
fnm install --lts
```

### 4. Install the Codex CLI

Run:

```bash
npm i -g @openai/codex
```

### 5. Install `cxhere`

`cxhere` is an extra helper tool from me, open source.

Run:

```bash
curl -fsSL https://raw.githubusercontent.com/moorage/cxhere/main/install.sh | bash
```

## Quick Check

After setup, these commands should work:

```bash
git --version
brew --version
fnm --version
node --version
npm --version
codex --version
```
