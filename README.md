Test npm scripts behaviors

- https://docs.npmjs.com/cli/v6/using-npm/scripts
- https://docs.npmjs.com/cli/v7/using-npm/scripts

Installing self dependencies:

```
$ npm -v
6.14.12
$ node -v
v14.16.1
$ npm i

> @jchip/test-npm-scripts@1.0.0 preinstall /Users/home/projects/test-npm-scripts
> echo Hello from npm script preinstall && pwd

Hello from npm script preinstall
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 install /Users/home/projects/test-npm-scripts
> echo Hello from npm script install && pwd

Hello from npm script install
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 postinstall /Users/home/projects/test-npm-scripts
> echo Hello from npm script postinstall && pwd

Hello from npm script postinstall
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 prepare /Users/home/projects/test-npm-scripts
> echo Hello from npm script prepare && pwd

Hello from npm script prepare
/Users/home/projects/test-npm-scripts
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN @jchip/test-npm-scripts@1.0.0 No repository field.

added 1 package and audited 1 package in 0.529s
found 0 vulnerabilities
```

Publishing:

```
$ npm -v
6.14.12
$ node -v
v14.16.1
$ npm publish

> @jchip/test-npm-scripts@1.0.0 prepare .
> echo Hello from npm script prepare && pwd

Hello from npm script prepare
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 prepublishOnly .
> echo Hello from npm script prepublishOnly && pwd

Hello from npm script prepublishOnly
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 prepack .
> echo Hello from npm script prepack && pwd

Hello from npm script prepack
/Users/home/projects/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 postpack .
> echo Hello from npm script postpack && pwd

Hello from npm script postpack
/Users/home/projects/test-npm-scripts
npm notice
npm notice 📦  @jchip/test-npm-scripts@1.0.0
npm notice === Tarball Contents ===
npm notice 22B  index.js
npm notice 745B package.json
npm notice 100B README.md
npm notice === Tarball Details ===
npm notice name:          @jchip/test-npm-scripts
npm notice version:       1.0.0
npm notice package size:  491 B
npm notice unpacked size: 867 B
npm notice shasum:        1620e5ef65914e225d2e5aeae862df021a92e2e9
npm notice integrity:     sha512-5NRH9MqPGdKTp[...]Li9dL4XtmhDIA==
npm notice total files:   3
npm notice
+ @jchip/test-npm-scripts@1.0.0
```

Installing as dep:

```
$ npm -v
6.14.12
$ node -v
v14.16.1
$ mkdir test-npm1 && cd test-npm1 && npm init --yes && npm i @jchip/test-npm-scripts
Wrote to /Users/home/projects/test-npm1/package.json:

{
  "name": "test-npm1",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC"
}



> @jchip/test-npm-scripts@1.0.0 preinstall /Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts
> echo Hello from npm script preinstall && pwd

Hello from npm script preinstall
/Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 install /Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts
> echo Hello from npm script install && pwd

Hello from npm script install
/Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts

> @jchip/test-npm-scripts@1.0.0 postinstall /Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts
> echo Hello from npm script postinstall && pwd

Hello from npm script postinstall
/Users/home/projects/test-npm1/node_modules/@jchip/test-npm-scripts
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN test-npm1@1.0.0 No description
npm WARN test-npm1@1.0.0 No repository field.

+ @jchip/test-npm-scripts@1.0.0
added 1 package and audited 1 package in 0.61s
found 0 vulnerabilities
```
