# NPM exploration
My personal project for exploring the Node Package Manager (NPM). 
NPM have excellent [documnetation](https://docs.npmjs.com/getting-started/what-is-npm), but this document
describes the commands I used the most to start out with.

## Install packages
Install a new package that should only used during development: 

    npm install [package] --save-dev

The package will be added to the `devDependencies` section of the `package.json` file.

    npm install [package]@[version]     # Install a specific version of a package.
    npm install [package] -g            # Install a package globally e.g. gulb.js

To install packages defined in a `package.json` file for an existing project:

    npm install

## Uninstall packages
Uninstall package and remove the dependency from the `package.json` file

    npm uninstall [package]

## Listing packages
    npm list
    npm list --depth 0      # Limit the dependency tree display depth
    npm list --dev          # List only dev packages
    npm list -g --depth 0   # List global packages
    
## Updating packages
If packages are defined in `package.json` using [ranges](https://docs.npmjs.com/getting-started/semantic-versioning#semver-for-consumers)
`npm update` will update the packages with respect to the given ranges.  

    npm update [package]    # Update only a single package. Usefull when testing if updating a package breaks something.