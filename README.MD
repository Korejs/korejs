[![Kore.js Logo](https://github.com/Korejs/korejs/raw/master/misc/images/Kore.js-Logo.png)
[![JavaScript Style Guide](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)
[![forthebadge](http://forthebadge.com/images/badges/contains-cat-gifs.svg)](https://github.com/Korejs)
[![forthebadge](http://forthebadge.com/images/badges/built-by-hipsters.svg)](https://github.com/Korejs)

## A modern full stack JS REST and realtime API layer, inspired by Feathers

Kore.js is a real-time, micro-service web framework for NodeJS that gives you control over your data via RESTful resources, sockets, GraphQL etc.

## Why?
Since Node v.7 is here we have the cutting edge features of ES7, like async-await. However [Feathers.js](https://korejs.com/) doesn't support them.
So Koa.js is here to help.

## See what makes Kore.js different

### Cutting edge, solid, and 100% JavaScript

Built using async-await and ES7 features, Kore.js is a tiny, fully compatible wrapper over Koa.js and Socket.io / Primus

### Universal
Kore.js can be used in the browser, React Native and server side with Node.js. Using the Kore.js client you can quickly add authentication, share code between your server and client, and easily make your apps real-time.

### Framework Friendly
Kore.js easily integrates with any client side framework. Whether it be React, VueJS, Choo or Angular - it doesn't matter!

### Service Oriented
Kore.js gives you the structure to build service oriented apps from day one. When you eventually need to split up your app into microservices it’s an easy transition and your Kore.js apps can scale painlessly.

### Instant Real-time REST APIs
Kore.js provides instant CRUD functionality via Services, exposing both a RESTful API and real-time backend automatically through Socket.io or Primus.

### Datastore Agnostic
Kore.js has adapters for 15+ data sources out of the box, including MongoDB, Postgres, RethinkDB and S3. You can have multiple datastores in a single app and swap them out painlessly due to our consistent query interface.

### Flexible Plugins
Kore.js is a “batteries included but easily swappable framework”. We have entirely optional plugins that allow you to implement 300+ Passport authentication providers, flexible authorization permissions and things like SMS or email messaging out of the box. Include exactly what you need. No more, no less.


## Getting Started

1. Make sure you have [NodeJS](https://nodejs.org/)(v.6+) and [npm](https://www.npmjs.com/) installed.
2. Install your dependencies

    ```
    ./install.sh
    ```

3. Start your backend server

    ```
    ./dev-server.sh -b
    ./dev-server.sh -b -i  -- for inspection of backend via Chrome Dev Toos
    ```
    You can install [NIM extension](https://chrome.google.com/webstore/detail/nim-node-inspector-manage/gnhhdgbaldcilmgcpfddgdbkhjohddkj "Node Inspector Manager") for better development experience

4. Start your client server

    ```
    ./dev-server.sh -f
    ```

Development environment will use `http://localhost/3030` for backend server and `http://localhost/3000` for webpack-dev-server.

Both of servers using `watch` and will automatically reload on file changes

Keep in mind that we using `NODE_PATH=./src` for webpack-dev-server, so we can import modules like this:

 ````
 import attachToDOMNode from 'core/root'
 ````

instead of this:

 ````
 import attachToDOMNode from '../../../core/root'
 ````

## Testing

Simply run `npm test` and all your tests in the `test/` directory will be run.

## Building

Run `build.sh` script with `--host <HOST_NAME_WITH_PORT>` parameter.

`````
./build.sh -h http://localhost:3030
`````

Build results will be
moved to the `public/` folder.


## Scaffolding

Feathers has a powerful command line interface. Here are a few things it can do:

```
$ npm install -g korejs-cli             # Install Feathers CLI

$ korejs                                # Access korejs console
$ korejs generate service               # Generate a new Service
$ korejs generate hook                  # Generate a new Hook
$ korejs generate model                 # Generate a new Model
$ korejs help                           # Show all commands
```

## Style guides

We are using [JavaScript Standard Style](https://standardjs.com/) as linter and style guide for better consistency of our code.
````
"eslint": "^3.17.1",
````
Before pull request the code must not have linting errors and must have as less warnings as possible

### Misc
All repetitive code of React component in examples should go to one separate method
All conditional code of React component should have its own method, prefixed with `render`, for ex: `renderBody()` or `renderForm()`

## Git

## How to contribute

## List of contributors

## Misc

```

```

## Help

For more information on all the things you can do with Feathers visit [docs.korejs.org](docs.korejs.org).

## Versioning

We use [Semantic Versioning](http://semver.org/)

Given a version number MAJOR.MINOR.PATCH, increment the:

* MAJOR version when you make incompatible API changes,
* MINOR version when you add functionality in a backwards-compatible manner, and
* PATCH version when you make backwards-compatible bug fixes.
* Additional labels for pre-release and build metadata are available as extensions to the MAJOR.MINOR.PATCH format.

## Changelog

__0.0.1__

- Initial commit

## License

MIT
