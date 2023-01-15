# GYM PAGE

## About Project
It is a simple and stylish GYM Page made with HTML,CSS and JS. IT consist of three pages- Home,About,Contact. The code is very simple and easy to understand. Anyone with basic knowledge of front-end development can easily handle it and make changes according to his/her requirements.

<hr>

## Requirements

For development, you will only need Node.js installed on your environement.
And please use the appropriate [Editorconfig](http://editorconfig.org/) plugin for your Editor (not mandatory).
<hr>
### Node

[Node](http://nodejs.org/) is really easy to install & now include [NPM](https://npmjs.org/).
You should be able to run the following command after the installation procedure
below.

    $ node --version
    v0.10.24

    $ npm --version
    1.3.21
<hr>
#### Node installation on OS X

You will need to use a Terminal. On OS X, you can find the default terminal in
`/Applications/Utilities/Terminal.app`.

Please install [Homebrew](http://brew.sh/) if it's not already done with the following command.

    $ ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"

If everything when fine, you should run

    brew install node
<hr>
#### Node installation on Linux

    sudo apt-get install python-software-properties
    sudo add-apt-repository ppa:chris-lea/node.js
    sudo apt-get update
    sudo apt-get install nodejs
<hr>
#### Node installation on Windows

Just go on [official Node.js website](http://nodejs.org/) & grab the installer.
Also, be sure to have `git` available in your PATH, `npm` might need it.

---
<hr>
## Install

    $ git clone https://github.com/ORG/Nitin-Pikhwal/GYM-PAGE.git
    $ cd GYM-PAGE
    $ npm install
<hr>
## Simple build for production

    $ npm run build
<hr>
## Update sources

Some packages usages might change so you should run `npm prune` & `npm install` often.
A common way to update is by doing

    $ git pull
    $ npm prune
    $ npm install

To run those 3 commands you can just do

    $ npm run pull

*Note:* Unix user can just link the `git-hooks/post-merge`:
<hr>
## Enable git hooks (unix only :/)

    $ npm run create-hook-symlinks

### `post-merge` (≃ `npm install`)

This hook will `npm prune && npm install` each time you `git pull` something if the `package.json` has been modified.

### `pre-commit` (≃ `npm test`)

This hook will just ensure you will commit something not broken bye pruning npm packages not in the `package.json` & eventually reinstall missings/not correctly removed packages.
Then it will try a production build.

---
<hr>
## Languages & tools

### HTML

- [Jade](http://jade-lang.com/) for some templating.

### JavaScript

- [JSHint](http://www.jshint.com/docs/) is used to prevent JavaScript error.
- [JSCS](https://npmjs.org/package/jscs) is used to check coding conventions.
- [Browserify](http://browserify.org/) to handle allow us to write our client-side scripts with [es6 syntax](http://es6.github.io/) thanks to [es6ify](https://github.com/thlorenz/es6ify).

### CSS

- [cssnext](http://cssnext.putaindecode.io) is used to write futureproof CSS for CSS vendor prefix under the hood).

Autoprefixer is included and use [caniuse.com](http://caniuse.com/) database to avoid outdated prefixes. You can forget CSS prefixes NOW.
<hr>
### Static server with Livereload

The app embed for development a static connect server with livereload plugged.
So each time you start the app, you get automatic refresh in the browser whenever you update a file.
