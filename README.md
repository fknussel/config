# Developer's macOS Fresh Install

This document describes how I set up my development environment on a new MacBook or iMac. 

## System Preferences

**Apple icon > System Preferences:**

* Dock > Automatically hide and show the Dock

## Host Name

```
sudo scutil --set HostName <new-host-name>
```

## Workspace

```
mkdir ~/workspace
```

## General Dev Tools

* [iTerm2](https://www.iterm2.com/)
* [Git](http://git-scm.com/)
* [VirtualBox](https://www.virtualbox.org/)
* [CyberDuck](https://cyberduck.io/)
* [Sequel Pro](http://www.sequelpro.com/)
* [Postman](https://www.getpostman.com/)
* [GitUp](http://gitup.co/) (useful for going through `diff`'s)
* [Charles Proxy](https://www.charlesproxy.com/)

## Front End Dev Tools

* [nvm](https://github.com/creationix/nvm)
* [Sublime Text](https://www.sublimetext.com/)

### Sublime Text Plugins

Install the following Sublime packages via [Package Control](https://packagecontrol.io/):

* [Cobalt2](https://github.com/wesbos/cobalt2) or [Material Theme](https://github.com/equinusocio/material-theme)
* [EditorConfig](http://editorconfig.org/)
* [Babel](https://github.com/babel/babel-sublime) (ES6 and JSX syntax highlighting)
* [SCSS](https://github.com/MarioRicalde/SCSS.tmbundle) (SCSS syntax highlighting)
* [DocBlockr](https://github.com/spadgos/sublime-jsdocs)
* [Pretty JSON](https://github.com/dzhibas/SublimePrettyJson)
* [SublimeLinter](http://www.sublimelinter.com/)
* [SublimeLinter-contrib-eslint](https://github.com/roadhump/SublimeLinter-eslint) (dependency: `npm install -g eslint`)
* [SublimeLinter-contrib-sass-lint](https://github.com/skovhus/SublimeLinter-contrib-sass-lint) (dependency: `npm install -g sass-lint`)

## Android Dev Tools

* [Java Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/)
* [Android Studio](https://developer.android.com/studio/) (let AS get you an appropriate version of the Android SDK)

## Haskell Dev Tools

* [Haskell for Mac](http://haskellformac.com/)

## Configuration Files and Git Scripts

Place these scripts on your home (`~`) directory:

* [`.bash_profile`](./.bash_profile)
* [`.gitconfig`](./.gitconfig)
* [See repository status in your prompt](https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh)
* [Git completion support](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash)

## Misc Tools

* [iA Writer](https://ia.net/writer)
* [The Unarchiver](http://unarchiver.c3.cx/unarchiver)
* [Magnet](http://magnet.crowdcafe.com/)
* [f.lux](https://justgetflux.com/)
* [Quickly](https://philmarell.com/quickly/)

## Built-in Local Apache Server

To enable PHP edit this file:

```
sudo vim /etc/apache2/httpd.conf
```

and uncomment this line:

```
LoadModule php5_module libexec/apache2/libphp5.so
```

Grant writing privileges:

```
sudo chown -R fknussel: /Library/WebServer/Documents
sudo chmod -R a+wx /Library/WebServer/Documents
```

Restart Apache.
