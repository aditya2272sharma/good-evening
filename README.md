# Snapbizweb

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.2.7.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
Before running the tests make sure you are serving the app via `ng serve`.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
 
## Angular CLI Deployment: Host Your Angular 2 App on Heroku
URL: https://medium.com/@ryanchenkie_40935/angular-cli-deployment-host-your-angular-2-app-on-heroku-3f266f13f352

* Set the `@angular/cli` module as dependency. Dev dependencies are not installed in Prod environment.
* Create a static server e.g. `server.js` in Node.
* Update the `Procfile`. Set `web: node server.js` in it.
* Add enignes information - set whatever node & npm versions you're using locally
* Force SSL for heroku

## NodeJS & NPM installation, Yarn
* Use `nvm` for installing multiple versions of the node executable
* With `nvm`, install the node version which has **LTS** i.e. **Long Term Support**
* `nvm ls` will list down all versions currently on your system 
* `nvm install --lts=carbon` - run this command to install `v8.9.2`
* Read more about LTS - https://github.com/creationix/nvm/blob/master/README.md#long-term-support
* **Note** - The version number might differ. The command above will always pick up the latest version in the LTS line.
* **Yarn Engine warnings** - Yarn might throw warnings when you work with 8.9.3.
  * So use - `--ignore-engines`
  * also, add `--ignore-scripts` to avoid building each time
  * Final command:
    * `yarn install --ignore-engines --ignore-scripts`

**Example:** For my case, it installed `v8.9.3`

```js
Installing with latest version of LTS line: carbon
Downloading and installing node v8.9.3...
Downloading https://nodejs.org/dist/v8.9.3/node-v8.9.3-linux-x64.tar.xz...
######################################################################## 100.0%
Computing checksum with sha256sum
Checksums matched!
Now using node v8.9.3 (npm v5.5.1)
``` 

## Heroku

* This app is a replica of https://github.com/angular/angular-cli/blob/master/package.json
* The instructions for building a heroku angular 2 app was found on https://medium.com/@ryanchenkie_40935/angular-cli-deployment-host-your-angular-2-app-on-heroku-3f266f13f352


### Understand Heroku Buildpack for NodeJS

* https://elements.heroku.com/buildpacks/heroku/heroku-buildpack-nodejs
* Download: `https://elements.heroku.com/buildpacks/heroku/heroku-buildpack-nodejs`
* Check Logs (order of priority - high to low):
  * `heroku logs --source app`
  * `heroku logs --tail`
  * `heroku logs --source app --dyno api --tail`
* https://blog.angularindepth.com/making-your-angular-2-library-statically-analyzable-for-aot-e1c6f3ebedd5



 
