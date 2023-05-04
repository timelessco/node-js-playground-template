# Development

## Table of Contents

- [Development](#development)
  - [Table of Contents](#table-of-contents)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
  - [Configuration](#configuration)
  - [Installing the dependencies](#installing-the-dependencies)
  - [Running the project locally](#running-the-project-locally)
  - [Building the project](#building-the-project)
  - [More DX scripts](#more-dx-scripts)
    - [Prettier](#prettier)
    - [Eslint](#eslint)
    - [Markdown](#markdown)
    - [Check Types](#check-types)
    - [Check unused dependencies, exports \& types](#check-unused-dependencies-exports--types)
    - [Check Spelling](#check-spelling)
    - [Check package.json](#check-packagejson)
    - [Test](#test)
    - [Contributions](#contributions)

## Prerequisites

Before you get started, you will need to have the following tools installed on
your machine:

- **[Node.js][1]** (version 12 or later)
- **[pnpm][2]** (version 5 or later) or **[npm][3]** or **[yarn][4]** (version 6
  or later)
- **[Git][5]** (optional, but recommended for version control)

> This repository includes a list of suggested VS Code extensions. It's a good
> idea to use [VS Code][6] and accept its suggestion to install them, as they'll
> help with development.

## Getting Started

## Configuration

The project uses environmental variables for configuration. You can set the
environmental variables in a **`.env.development`** & **`.env.production`**
files in the root directory of the project. These files should contain key-value
pairs in the following format:

- **`NODE_ENV`** (required): The environment in which the project is running.
  This can be either `development` or `production`.

> Adding a new environmental variable requires aa addition in the
> `src/config/validateEnvironment.ts` file and a new entry in the global type
> `interface NodeJS.ProcessEnv`.

## Installing the dependencies

After you have set the environmental variables, you can run the project locally
by

```shell
git clone https://github.com/timelessco/node-ts-app
cd node-ts-app
pnpm install
```

This will download and install all the required dependencies for the project.

## Running the project locally

```bash
pnpm dev
```

This will watch the `src` directory for changes and recompile the project on
every change using `nodemon`.

You can start editing the page by modifying `src/index.ts`.

## Building the project

You can use the below command to build the production-ready version of the
project.

```bash
pnpm build
```

## More DX scripts

> Check for all the below errors in one command using [Turbo Repo][7]

`pnpm lint`

> AutoFix all the linting errors in one command using [Turbo Repo][7]

`pnpm format`

### Prettier

[Prettier][8] is used to format code. It should be applied automatically when
you save files in VS Code or make a Git commit.

> Check the formatting errors

`pnpm lint:prettier`

> AutoFix the formatting errors

`pnpm format:prettier`

> This package includes several forms of linting to enforce consistent code
> quality and styling. Each should be shown in VS Code, and can be run manually
> on the command-line:

### Eslint

Extends all the necessary rulesets from [eslint-config-canonical][9] for the
project that lints JavaScript and TypeScript source files

> Check for the linting errors

`pnpm lint:eslint`

> AutoFix the linting errors

`pnpm format:eslint`

### Markdown

([Markdownlint][10]): Checks all Markdown files

> Check the markdown linting errors

`pnpm lint:md`

> AutoFix the markdown linting errors

`pnpm format:md`

### Check Types

([TypeScript][11]): Checks all TypeScript files

> Check TypeScript types

`pnpm lint:types`

### Check unused dependencies, exports & types

([knip][12]): Checks all unused dependencies, exports & types

> Check the spelling errors

`pnpm lint:knip`

### Check Spelling

([cspell][13]): Spell checks across all source files

> Check the spelling errors

`pnpm lint:spelling`

> Populate `project-words.txt` with the words that are not in the dictionary &
> fix

`pnpm populate:dictionary`

### Check package.json

([npm-package-json-lint][14]): Lints the `package.json` file

> Check the package.json linting errors

`pnpm lint:package-json`

### Test

> Run the test suite

`pnpm test`

### Contributions

([all-contributors][15]): ✨ Recognize all contributors, not just the ones who
push code ✨

> Add new contributors

`pnpm contributors:add`

> Generate the contributors list

`pnpm contributors:generate`

[1]: https://nodejs.org/en/
[2]: https://pnpm.io/
[3]: https://www.npmjs.com/
[4]: https://yarnpkg.com/
[5]: https://git-scm.com/
[6]: https://code.visualstudio.com
[7]: https://turbo.build/repo
[8]: https://prettier.io
[9]: https://github.com/gajus/eslint-config-canonical
[10]: https://github.com/DavidAnson/markdownlint
[11]: https://www.typescriptlang.org/
[12]: https://github.com/webpro/knip
[13]: https://cspell.org
[14]: https://npmpackagejsonlint.org/
[15]: https://github.com/all-contributors/all-contributors
