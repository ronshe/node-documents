# Node CLI

## Introduction
There are three different common interfaces:
1. Command line with parameters and flags [(#)](#command-line-with-parameters-and-flags)
2. Interactive UI [(#)](#interactive-ui)
3. Shell like [(#)](#shell-like)

[Related libraries](#related-libraries)

## Command line with parameters and flags
Stateless application. Each execution runs one command and stops. Next execution does not depend on the previous one, but it might depend on state of the storage like files or database.

### Example:
```
$ my-cli --help
$ my-cli create --type json --output out-file.json
```
### Known applications with similar behavior:
* git

### Libraries:
* https://oclif.io/

### Articles:
* https://timber.io/blog/creating-a-real-world-cli-app-with-node/

## Interactive UI
UI interface. Has selection (single/multiple), inputs, messages, spinner, etc. 

### Example:
```
$ my-ui
Username: user
Password: ******
What would you like to do:
  *  Connect
  *  Disconnect
  *  Send data
  *  Receive data
  *> Exit
Good bye
$
```
### Known applications with similar behavior:
* npm init

### Libraries:
* [Commander.js](https://www.npmjs.com/package/commander) - Command-line library.
* [Inquirer.js](https://www.npmjs.com/package/inquirer) - Command-line user interfaces.

### Articles:
* https://scotch.io/tutorials/build-an-interactive-command-line-application-with-nodejs
* TypeScript: https://itnext.io/how-to-create-your-own-typescript-cli-with-node-js-1faf7095ef89

## Shell like
Shell like interactive command line

### Example:
```
$ my-shell
shell> help
help          Prints help
connect       Connects to the server
disconnect    Disconnects from the server
send          Send data
receive       Receive data
shell> connect https://go.home --user root --password kji7TYKI67t6tTG
...... Connected
shell> send --file messages.txt
... Sent OK
shell> exit
$
```
### Known applications with similar behavior:
* mysql
* mongo

### Libraries:
* [vorpal](http://vorpal.js.org/) - Good examples and documentation, build in help and autocompletion.
* [GlueGun](https://infinitered.github.io/gluegun/) - Looks very complete, but no examples are given.
### Articles:
* https://www.sitepoint.com/javascript-command-line-interface-cli-node-js/

## Related libraries
* [Prompts](https://www.npmjs.com/package/prompts) - interactive prompts.
* [Yargs](https://www.npmjs.com/package/yargs) - Parsing cli flags and parameters
* [minimist](https://www.npmjs.com/package/minimist) - Parse argument options.
* [chalk](https://www.npmjs.com/package/chalk) - Terminal string styling and coloring.
* [Colors](https://www.npmjs.com/package/colors) - Terminal string styling and coloring.
