# bootstrap - [AngularJS](http://angularjs.org/) directives specific to [twitter bootstrap](http://twitter.github.com/bootstrap/)

***

[![Build Status](https://secure.travis-ci.org/angular-ui/bootstrap.png)](http://travis-ci.org/angular-ui/bootstrap)

## Project philosophy

### Native, lightweight directives

We are aiming at providing a set of AngularJS directives based on Twitter Bootstrap's markup and CSS. The goal is to provide **native AngularJS directives** without any dependency on jQuery or Bootstrap's JavaScript.
It is often better to rewrite an existing JavaScript code and create a new, pure AngularJS directive. Most of the time the resulting directive is smaller as compared to the orginal JavaScript code size and better integrated into the AngularJS ecosystem.

### Customizability

All the directives in this repository should have their markup externalized as templates (loaded via `templateUrl`). In practice it means that you can **customize directive's markup at will**. One could even imagine providing a non-Boostrap version of the templates!

### Take what you need and not more

Each directive has its own AngularJS module without any dependencies on other modules or third-pary JavaScript code. In practice it means that you can **just grab the code for the directives you need** and you are not obliged to drag the whole repository.

### Quality and stability

Directives should work. All the time and in all browsers. This is why all the directives have a comprehensive suite of unit tests. All the automated tests are executed on each checkin in several browsers: Chrome, ChromeCanary, Firefox, Opera, Safari, IE9.
In fact we are fortunate enough to **benefit from the same testing infrastructure as AngularJS**!

## Contributing to the project

We are always looking for the quality contributions! Please check the [CONTRIBUTING.md](bootstrap/blob/master/CONTRIBUTING.md) for the contribution guidelines.

### Development
#### Prepare your environment
* Install [Node.js](http://nodejs.org/) and NPM (should come with)
* Install global dev dependencies: `npm install -g grunt testacular`
* Instal local dev dependencies: `npm install` while current directory is bootstrap repo

#### Run unit tests
* Start testacular server: `grunt server`
* Run test: `grunt test-run`

#### Before commit
* Build the whole project: `grunt` - this will run `lint`, `test`, and `concat` targets

### Release
* Bump up version number in `package.json`
* Commit the version change with the following message: `chore(release): [versio number]`
* tag
* push changes and a tag (`git push --tags`)
* switch to the `gh-pages` branch: `git checkout gh-pages`
* copy content of the dist folder to the main folder
* Commit the version change with the following message: `chore(release): [versio number]`
* push changes
* switch back to the `main branch` and modify `package.json` to bump up version for the next iteration
* commit (`chore(release): starting [versio number]`) and push

Well done! (If you don't like repeating yourself open a PR with a grunt task taking care of the above!)
