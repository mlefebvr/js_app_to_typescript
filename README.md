# Convert JS app to Typescript

Converting a JavaScript app to Typescript is simple. 

## The app
This document assumes that you have a working NodeJS application. It also assumes that the
source files for the application are located in the src/ sub-directory.

An example application can be found [here]

## Install the dependancies

Inside your JavaScript project, install the dependencies for Typescript:

- ts-node
- typescript

```
$ npm i -D ts-node typescript
```

You may need to install type packages for the libraries that your project uses (ie: @types/express if your project uses express)

## Setup the compiler

First setup the compiler by running

```
npx tsc --init 
```

Once done, open the generated tsconfig.json file with your code editor and apply the following changes:

- Inside "compilerOptions"
  - Set the "target" attribute to the version of JavaScript to transpile to (ie: esnext, es2016)
  - Set the "outDir" attribute to the destination where to generate the transpiled files (ie: build/)
  - Set the "rootDir" attribute to the directory where your source files are stored (ie: src/)
- Add the following attributes at the root of the file (alongside "compilerOptions")
  - include: ["src/**/*.ts"]
  - exclude: ["node_modules"]

