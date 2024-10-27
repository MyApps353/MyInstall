# My Install Package

This package introduces a set of custom npm commands designed to simplify package installation, aliasing paths, and automatic updates to specified documentation files with installation information.

## Table of Contents

- [Features](#features)
- [Config File Example](#config-file-example)
- [Installation](#installation)
- [Usage](#usage)
  - [Initialize the Package](#1-initialize-the-package)
  - [Set Default Path](#2-set-default-path)
  - [Add Alias](#3-add-alias)
  - [Install a Package and Log](#4-install-a-package-and-log)
- [Development](#development)
- [License](#license)

## Features

- Custom Install Command  
  Run `npm myinstall:<PATH OR ALIAS>` to install an npm package and automatically log it in the specified file, formatted as defined in the configuration.

- Set Default Path  
  Use `npm myinstall -set-default <PATH>` to define a default path for `myinstall` commands.

- Add Path Alias  
  Add a shortcut for paths with `npm myinstall -add <ALIAS>:<PATH>`. Aliases can be used with `myinstall` commands.

- Shortcut Command  
  `npm mi` works as a shortcut for the `myinstall` command.

- Configurable Output  
  Control how package installations are logged with a `myinstall.config.json` file. Define headers, content structure, and placeholders to match your desired output style.

## Config File Example

A configuration file (`myinstall.config.json`) allows for fully customizable outputs:

```json
{
  "header": "## Packages used",
  "content": " - <#>"
}
```

`<#>` will be replaced by the package name.

## Installation

Install the package globally or locally depending on your needs:

`npm install -g custom-npm-command-package`

## Usage

1. Initialize the Package  
   Run `npm myinstall init` to create a default configuration file (`myinstall.config.json`).

2. Set Default Path  
   Set a default path for logging installations with:
   `npm myinstall -set-default <PATH>`

3. Add Alias  
   Add an alias for a path:
   `npm myinstall -add <ALIAS>:<PATH>`

4. Install a Package and Log  
   Use the command to install a package and log it as defined in your config file:
   `npm myinstall <PACKAGE_NAME>`

   Shortcut: You can also use `npm mi <PACKAGE_NAME>`.

## Development

To contribute to this package:

1. Fork and clone the repository.
2. Make your changes.
3. Submit a pull request.

Thank you for helping improve this project! If you want to support ongoing development, consider [buying me a coffee](https://buymeacoffee.com/myapps353).

## License

This project is licensed under the MIT License. See the LICENSE.md file for details.
