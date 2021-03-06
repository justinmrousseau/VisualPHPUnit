[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/VisualPHPUnit/VisualPHPUnit/badges/quality-score.png)]
(https://scrutinizer-ci.com/g/VisualPHPUnit/VisualPHPUnit/)
[![Build Status](https://travis-ci.org/VisualPHPUnit/VisualPHPUnit.svg)](https://travis-ci.org/VisualPHPUnit/VisualPHPUnit)
[![Dependency Status](https://www.versioneye.com/user/projects/55f547b3a4155f00090005b5/badge.svg?style=flat)](https://www.versioneye.com/user/projects/55f547b3a4155f00090005b5)
[![Project Stats](https://www.openhub.net/p/VisualPHPUnit/widgets/project_thin_badge.gif)](https://www.openhub.net/p/VisualPHPUnit)
[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%205.6-8892BF.svg?style=flat-square)](https://php.net/)
[![codecov.io](http://codecov.io/github/VisualPHPUnit/VisualPHPUnit/coverage.svg)](http://codecov.io/github/VisualPHPUnit/VisualPHPUnit)
![Version Eye](http://php-eye.com/badge/visualphpunit/visualphpunit/tested.svg)
[![PHPPackages Rank](http://phppackages.org/p/visualphpunit/visualphpunit/badge/rank.svg)](http://phppackages.org/p/visualphpunit/visualphpunit)

# VisualPHPUnit

VisualPHPUnit is a visual front-end for PHPUnit.

Version [3.0.0](https://github.com/VisualPHPUnit/VisualPHPUnit/releases/tag/v3.0.0) is the latest and greatest but [2.3.2](https://github.com/VisualPHPUnit/VisualPHPUnit/releases/tag/v2.3.2) is also working just fine.

## Versions

* [1.x](https://github.com/VisualPHPUnit/VisualPHPUnit/tree/1.x) Initial concept and code by [Matt Mueller](https://github.com/matthewmueller)
* [2.x](https://github.com/VisualPHPUnit/VisualPHPUnit/tree/2.x) A complete rewrite by [Nick Sinopoli](https://github.com/NSinopoli)
* [3.x](https://github.com/VisualPHPUnit/VisualPHPUnit/tree/3.x) A complete rewrite by [Johannes Skov Frandsen](https://github.com/localgod)

##Setup

 * Checkout or download VisualPHPUnit
 * Run composer.php to install php dependecies.
 * Run npm install
 * Run bower install
 * Run `./bin/vpu -c vpu.json -s` to start VisualPHPUnit with the build-in php server.
 * Run `./bin/vpu -c vpu.json -t` to stop VisualPHPUnit with the build-in php server.

You may browse localhost:8000 to access the test suites.

You can update `./vpu.json` to add additional test suites.

You may run tests from the console like this `./bin/vpu -c vpu.json testfile.php`. You may append `-a` to archive your test results. 

## Development

### Frontend
The frontend is a single-page javascript application ([SPA](https://en.wikipedia.org/wiki/Single-page_application)) based on [Angularjs](https://angularjs.org/) and [Bootstrap](http://getbootstrap.com/). You will need [Node.js](https://nodejs.org/), [Npm](https://www.npmjs.com/), [Grunt](http://gruntjs.com/) and [Bower](http://bower.io/) to build the frontend.

### Backend
The backend is a REST application based on [Silex](http://silex.sensiolabs.org/). You will need [Composer](https://getcomposer.org/) to install relevant dependencies.You need [php](http://php.net/) >=5.6 to run VisualPHPUnit.


## Running VPU in dev mode

### Setup dependencies
```bash	
git clone git@github.com:VisualPHPUnit/VisualPHPUnit.git
git checkout 3.x
php -r "readfile('https://getcomposer.org/installer');" | php
php composer.phar install
npm install
bower install
```

## Start VPU in dev mode
You need two consoles for this setup, one for the frontend and one for the backend.
```bash
cd backend
php -S localhost:8001
cd ../app
grunt serve
```

## Running VPU at the Command Line

VPU can be run at the command line, making it possible to automate the generation of test results via cron.

You may append --help for options

### Usage

```bash
./bin/vpu
```

You may read more about VisualPHPUnit [here](http://visualphpunit.github.io/VisualPHPUnit/) or in the [wiki](https://github.com/VisualPHPUnit/VisualPHPUnit/wiki).
