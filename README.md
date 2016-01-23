![angular-express-header](https://cloud.githubusercontent.com/assets/1859381/8266502/d94e93ce-1731-11e5-9b9d-9b9e58c5369f.png)

[Angular Express](http://www.angular-express.com) boilerplate to start a Bootstrap only website without AngularJS.

Features:

- automatic compilation of ES6 with [Babel](https://babeljs.io/)
- pre-configured package management using [jspm](http://jspm.io/)
- dynamic module loading using the [SystemJS dynamic ES6 loader](https://github.com/systemjs/systemjs)
- pre-configured unit testing with [karma](http://karma-runner.github.io/), [mocha](http://mochajs.org/), [chai](http://chaijs.com/) and [PhantomJS](http://phantomjs.org/)
- powerful built-in server based on [Express 4](http://expressjs.com/) and [Harp](http://harpjs.com/) with preprocessor support for [Jade](http://jade-lang.com/), [Markdown](http://daringfireball.net/projects/markdown/), [EJS](http://www.embeddedjs.com/), [Coffeescript](http://coffeescript.org/), [Sass](http://sass-lang.com/), [LESS](http://lesscss.org/) and [Stylus](https://learnboost.github.io/stylus/).
- compile to HTML, CSS & JavaScript and host it anywhere
- customizable Bootstrap CSS framework

## How to get started

Ensure the [Angular Express CLI tool](https://github.com/angular-express/ngx-cli) is installed:

```bash
$ npm install -g ngx-cli
```

Create a new project directory:

```bash
$ mkdir project
$ cd project
```

Initialize the boilerplate:

```bash
$ ngx init -b bootstrap-only
```

Install third-party dependencies:

```bash
$ jspm install
$ npm install
```

Finally start the Angular Express server:

```bash
$ npm start
```

and navigate to: `<ip>:9000` in the browser.

## How the configuration works

The configuration is stored in configuration files in the `/config` directory.

It can be overriden and extended using the [node-config](https://github.com/lorenwest/node-config) rules:

```bash
# Default configuration
/config/default.js

# Production configuration
/config/production.js

# Local configuration
/config/local.js
```

See [configuration files](https://github.com/lorenwest/node-config/wiki/Configuration-Files) for more information.

## How to start the server

Start the server:

```bash
# Uses NODE_ENV of your environment
$ npm start
```

Start the server in development mode:

```bash
# Uses NODE_ENV=development
$ npm run development-server
```

Start the server in production mode:

```bash
# Update src/build.js
$ npm run build

# Start production server
# Uses NODE_ENV=production
$ npm run production-server
```

## How to compile to a static application

From the root of the project, run:

```bash
$ npm run compile
```

to compile static HTML, CSS and JavaScript in `dist`.

## How to use livereload during development

Ensure you have [BrowserSync](http://www.browsersync.io/) installed:

```bash
$ npm install -g browser-sync
```

From the root of the project, run:

```bash
$ browser-sync start --proxy localhost:9000 --files "src/**/*"
```

and navigate your browser to the BrowserSync url:

```bash
 --------------------------------------
       Local: http://localhost:3000
 --------------------------------------
          UI: http://localhost:3001
 --------------------------------------
```

## How to run unit tests

Make sure the Karma CLI is installed:

```bash
$ npm install -g karma-cli
```

To run the tests:

```bash
$ karma start
```

## License

[MIT](LICENSE)

## Change log

### v0.1.0

- Initial version
