# node-app-cheatsheet

## Intro

Hey there and thanks for checking out this repo.  My goal in creating this is to have a quick and simple reference guide for spinning up node projects.  This is not a super in-depth or comprehensive guide -- instead it's a straightforward "order of operations" and "don't forget this part" list.

## Getting Started

First off we'll make a digital home for our new stuff.  I like to go ahead and initialize it as a git repo straight off the bat, but that piece can be done in a few different ways.

- #### Andrew's preference:

Hop on Github and create your new repo.  Via terminal, navigate where you'd like it to live locally, and clone it down via your preferred method -- SSH, CLI, etc.

- #### Otherwise:

If you prefer, you can just make the folder and `git init` to establish it as a repo locally first, then connect when you eventually push.  I just like having an immediate connection between local and remote from the moment it's on my machine.

## NPM time

Now let's deal with Node/NPM.  In the terminal, having `cd`ed into the folder for the repo: 

- `code .` to get the directory open in VS Code
- `touch index.js` (or the appropriate Windows command) and take a peek at Code to confirm the file shows up
- `npm init -y` and take a look at Code again to confirm that node_modules and other npm boilerplate appears
- let's make sure we're not including those node_modules in our repo: run `echo "node_modules" >> .gitignore` to create your gitignore file and add the modules to its list

## Package stuff

Presumably there's a package -- or multiple packages -- that we're going to be including in this project.  Back in the terminal, let's run `npm i $packagename` to get it installed.  Once we see that it installs, let's go to our index.js to add the package: `const $package = require("$package");` will declare it in our JS and let us use whatever methods or tools we intend to employ.

## Moving on

You're pretty much set from here!  It's probably worth throwing a quick `git add .` and `git commit -m "Set up repo"` to have a clean slate committed before you start experimenting.  If you're using nodemon, run that as well to get the engine running in real time.  Next steps will be project/package specific, but if you've made it this far, you should be ready to rock and roll with your new project.  👍
