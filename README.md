powerbot-cli
============

CLI tool for Powerbot CMS projects

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/powerbot-cli.svg)](https://npmjs.org/package/powerbot-cli)
[![Downloads/week](https://img.shields.io/npm/dw/powerbot-cli.svg)](https://npmjs.org/package/powerbot-cli)
[![License](https://img.shields.io/npm/l/powerbot-cli.svg)](https://github.com/maxtomczyk/powerbot-cli/blob/master/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g powerbot-cli
$ powerbot COMMAND
running command...
$ powerbot (-v|--version|version)
powerbot-cli/2.0.0 darwin-x64 node-v10.15.1
$ powerbot --help [COMMAND]
USAGE
  $ powerbot COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`powerbot dev [MODULE]`](#powerbot-dev-module)
* [`powerbot env:list`](#powerbot-envlist)
* [`powerbot env:set [NAME]`](#powerbot-envset-name)
* [`powerbot env:unset [NAME]`](#powerbot-envunset-name)
* [`powerbot help [COMMAND]`](#powerbot-help-command)
* [`powerbot info`](#powerbot-info)
* [`powerbot init [NAME] [VERSION]`](#powerbot-init-name-version)
* [`powerbot language:add [NAME] [LOCALE]`](#powerbot-languageadd-name-locale)
* [`powerbot language:change [NAMEORLOCALETOCHANGE] [NEWLANGNAME] [NEWLANGLOCALE]`](#powerbot-languagechange-nameorlocaletochange-newlangname-newlanglocale)
* [`powerbot language:default [LANGORLOCALE]`](#powerbot-languagedefault-langorlocale)
* [`powerbot language:remove [NAMEORLOCALE]`](#powerbot-languageremove-nameorlocale)
* [`powerbot module [TYPE] [NAME]`](#powerbot-module-type-name)
* [`powerbot setup [FILE]`](#powerbot-setup-file)
* [`powerbot sync:attachments [SOURCE] [TARGET]`](#powerbot-syncattachments-source-target)
* [`powerbot sync:messages [FILE]`](#powerbot-syncmessages-file)

## `powerbot dev [MODULE]`

Starts commands set for project development

```
USAGE
  $ powerbot dev [MODULE]

DESCRIPTION
  As module accepts `cms` or `chatbot`
```

_See code: [src/commands/dev.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/dev.ts)_

## `powerbot env:list`

Lists environments for current project dir

```
USAGE
  $ powerbot env:list
```

_See code: [src/commands/env/list.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/env/list.ts)_

## `powerbot env:set [NAME]`

Manages environments (database connection params) used for sync module.

```
USAGE
  $ powerbot env:set [NAME]
```

_See code: [src/commands/env/set.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/env/set.ts)_

## `powerbot env:unset [NAME]`

Removes selected environment data from system

```
USAGE
  $ powerbot env:unset [NAME]
```

_See code: [src/commands/env/unset.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/env/unset.ts)_

## `powerbot help [COMMAND]`

display help for powerbot

```
USAGE
  $ powerbot help [COMMAND]

ARGUMENTS
  COMMAND  command to show help for

OPTIONS
  --all  see all commands in CLI
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v2.1.6/src/commands/help.ts)_

## `powerbot info`

Shows info about CLI and Powerbot CMS project

```
USAGE
  $ powerbot info
```

_See code: [src/commands/info.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/info.ts)_

## `powerbot init [NAME] [VERSION]`

Creates directory and initializes Powerbot CMS inside.

```
USAGE
  $ powerbot init [NAME] [VERSION]

DESCRIPTION
  As version you can use any release available on https://github.com/maxtomczyk/powerbot-cms/releases

ALIASES
  $ powerbot create
```

_See code: [src/commands/init.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/init.ts)_

## `powerbot language:add [NAME] [LOCALE]`

Helps to manage languages in Powerbot CMS

```
USAGE
  $ powerbot language:add [NAME] [LOCALE]

DESCRIPTION
  As locale you have to provide valid Facebook locale like en_US
```

_See code: [src/commands/language/add.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/language/add.ts)_

## `powerbot language:change [NAMEORLOCALETOCHANGE] [NEWLANGNAME] [NEWLANGLOCALE]`

Changes languege into another

```
USAGE
  $ powerbot language:change [NAMEORLOCALETOCHANGE] [NEWLANGNAME] [NEWLANGLOCALE]
```

_See code: [src/commands/language/change.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/language/change.ts)_

## `powerbot language:default [LANGORLOCALE]`

Sets passed language or locale to default

```
USAGE
  $ powerbot language:default [LANGORLOCALE]
```

_See code: [src/commands/language/default.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/language/default.ts)_

## `powerbot language:remove [NAMEORLOCALE]`

Removes language support from your chatbot.

```
USAGE
  $ powerbot language:remove [NAMEORLOCALE]
```

_See code: [src/commands/language/remove.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/language/remove.ts)_

## `powerbot module [TYPE] [NAME]`

Creates new component for CMS. Type paramter is `view` or `component`.

```
USAGE
  $ powerbot module [TYPE] [NAME]
```

_See code: [src/commands/module.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/module.ts)_

## `powerbot setup [FILE]`

Runs setup procedure like database import etc.

```
USAGE
  $ powerbot setup [FILE]
```

_See code: [src/commands/setup.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/setup.ts)_

## `powerbot sync:attachments [SOURCE] [TARGET]`

Copy content tables (attachments, messages) from source to target

```
USAGE
  $ powerbot sync:attachments [SOURCE] [TARGET]
```

_See code: [src/commands/sync/attachments.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/sync/attachments.ts)_

## `powerbot sync:messages [FILE]`

describe the command here

```
USAGE
  $ powerbot sync:messages [FILE]

OPTIONS
  -f, --force
  -h, --help       show CLI help
  -n, --name=name  name to print
```

_See code: [src/commands/sync/messages.ts](https://github.com/maxtomczyk/powerbot-cli/blob/v2.0.0/src/commands/sync/messages.ts)_
<!-- commandsstop -->