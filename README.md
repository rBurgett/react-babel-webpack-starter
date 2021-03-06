# react-babel-webpack-starter
This is a starter kit for building a completely front-end app using [React](https://facebook.github.io/react/), Babel and Webpack. Often you want an isomorphic solution, but sometimes you just need a drop-in webapp that does not require any changes to the server. That's what this is for. Build tasks are handled by Grunt using Babel for transpiling JSX and Webpack for bundling. Bootstrap is included (but easily removed). Flow type checking is also included, if you want to force static types. If you use eslint (which is highly recommended!), a configuration file is included with all the necessary plugins and configurations for this build setup.

## Getting Started
Install NPM dependencies:
```
> $ npm install
```

Build application: *(built application can then be found in the `dist` folder)*
```
> $ npm run build
```

Run development server:
```
> $ npm run dev-server
```

## Other NPM Scripts

Watch files and automatically rebuild application as you save changes:
```
> $ npm run watch
```

Build application for production: *(minifies files)*
```
> $ npm run build-production
```

Check code using [Flow](http://flowtype.org/) type checker:
```
> $ npm run flow
```

## Write in ES2015 (or ES6)
While transpiling JSX to JS, Babel will also convert any of the newer features of ES2015 into regular ES5 which can be run in any modern browser. Use scoped variables, arrow functions, string interpolation, modules, and classes today! **Note: All files in the `src` folder except for main.html need to be .jsx files as this is what the build process expects to find there.**

## Build view components using [React](https://facebook.github.io/react/)
The main starting point for the application is `/src/main.jsx`. Begin writing there. There are three sample React components included.

## Handle routing with [React Router](https://github.com/rackt/react-router)
A basic routing setup can be found in `./src/main.jsx`. The configuration is for front-end-only routing. It does not require any server configuration.

## Styling in [LESS](http://lesscss.org/)
[Bootstrap](http://bootstrapdocs.com/v3.3.5/docs/) is included for your base styles. All stylesheets are in LESS. Add your own imports or styles in `./less/main.less`. Comment-out any usused bootstrap imports in `./less/bootstrap/bootstrap.less`. LESS to CSS compiling is handled by Grunt.
(I have intentionally not included Bootstrap's JavaScript file because it forces a dependency on jQuery)

## Drop public assets into `public` folder
Everything in the `public` folder is copied directly into the `dist` folder during the build process. Any fonts, images, etc. should be placed here.
