# MEVN-Web-App

![Node 10](https://img.shields.io/badge/node-10.x.x-green.svg)
![VueJS 2](https://img.shields.io/badge/vuejs-2.3.x-green.svg)
![Webpack 4](https://img.shields.io/badge/webpack-4.17.x-green.svg)

Vue, Express, MongoDB full-stack JS Boilerplate

This is a full stack webapp boilerplate project with VueJS + ExpressJS + MongoDB. It is NOT an out-of-box project. 
I make it in order to create an up-to-date starter repo which contains all important functions (user signup, login, oauth, profile, ...etc) except the business-logic. So when neccessary I can create a new webapp and only need to develop the business logic.

*This is just my personal boilerplate, it may or may not be a good fit for your project(s).*
Inspired by [dstroot/skeleton](https://github.com/dstroot/skeleton) and [sahat/hackathon-starter](https://github.com/sahat/hackathon-starter)

(login: test/test1234 or sign-up)
## Features

**Server-side**
* [x] **[Node.JS](https://nodejs.org)** v10.x.x
* [x] **[Express](https://github.com/expressjs/express)**
* [x] [MongoDB](https://www.mongodb.com/) with [Mongoose](https://github.com/Automattic/mongoose)
* [x] [NodeMailer](https://github.com/nodemailer/nodemailer) with SMTP, MailGun or SendGrid
* [x] [Helmet](https://github.com/helmetjs/helmet)
* [x] [Express-validator](https://github.com/ctavan/express-validator)
* [x] [winston](https://github.com/winstonjs/winston) + 6 transports
* [x] **[GraphQL](http://graphql.org/)** with [Apollo stack](http://www.apollostack.com/)
* [x] [i18next](http://i18next.com/) as the internationalization ecosystem
* [x] **[HTTP/2 Server Push](https://en.wikipedia.org/wiki/HTTP/2_Server_Push)** with [netjet](https://github.com/cloudflare/netjet)
* [x] Bundled server-side code with [Webpack 2](https://webpack.github.io/)

**Client-side**
* [x] **[VueJS 2.x](https://github.com/vuejs/vue)**
* [x] [Vuex](https://github.com/vuejs/vuex)
* [x] [Vue-router](https://github.com/vuejs/vue-router)
* [x] [axios](https://github.com/mzabriskie/axios)
* [x] **[socket.io](https://github.com/socketio/socket.io) connection with namespaces & authorization**
* [x] [vue-websocket](https://github.com/wind757/vue-websocket)
* [x] [Jade](https://github.com/pugjs/pug)
* [x] **[Webpack 4](https://github.com/webpack/webpack)**
* [x] [SCSS](http://sass-lang.com/)
* [x] [PostCSS](https://github.com/postcss/postcss) with precss and autoprefixer
* [x] [Babel](https://babeljs.io/)
* [x] [Passwordless](https://www.sitepoint.com/passwordless-authentication-works/) mode
* [x] [Passport.JS](http://passportjs.org/)
	* Social signup/login with Facebook, Google, Twitter and Github
	* API key authentication for REST API calls
* [x] [Toastr](https://github.com/CodeSeven/toastr)
* [x] [vue-form-generator](https://github.com/wind757/vue-form-generator)

**Supported remote logging services**
* [x] [Papertrail](https://papertrailapp.com/)
* [x] [Graylog](https://www.graylog.org/)
* [x] [LogEntries](https://logentries.com/)
* [x] [Loggly](https://www.loggly.com/)
* [x] [Logsene](https://sematext.com/logsene/)
* [x] [Logz.io](http://logz.io/)

## Usage

Install dependencies
```
$ npm install
```
or
```
yarn
```

For development
```bash
$ npm run dev
```

Build web app scripts and styles:
```bash
$ npm run build
```

For production
```bash
$ npm start
```

## Docker

Building the images for the first time
```
$ docker-compose build
```

Starting the images
```
$ docker-compose up
```

## Directory structure
```txt
+---build
+---client
|   +---app
|   |   +---core
|   |   +---modules
|   |       +---demo
|   |       +---devices
|   |       +---home
|   |       +---posts
|   |       +---session
|   |                   
|   +---frontend
|   +---images
|   +---scss
|                   
+---data
+---logs
+---server
|   |   bundle.js
|   |   dev.js
|   |   index.js
|   +---applogic
|   |   +---libs
|   |   +---modules
|   |       +---counter
|   |       +---devices
|   |       +---posts
|   |       +---session
|   +---config
|   |       default.js
|   |       index.js
|   |       prod.js
|   |       test.js
|   |       
|   +---core
|   +---libs
|   +---locales
|   |   +---en
|   |   +---hu
|   +---models
|   |       user.js
|   +---public
|   +---routes
|   +---schema
|   +---services
|   +---views
+---tests
|
|   package.json
|   secrets.json

```

## Bundled server-side

If you want to bundle your NodeJS server-side code run webpack on server code with `npm run build && npm run build:server` command. It if was success, run the server: `npm run start:bundle`

If you want to export bundled version copy these folders & files to the new place:

```txt
- server
	- locales
	- public
	- views
	- bundle.js
- package.json
- config.js (optional)
```

Before start, you have to install production dependencies with npm: `npm install --production`
