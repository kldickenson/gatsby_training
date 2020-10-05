# About this training

A training workshop by [Mediacurrent](https://mediacurrent.com).

## Getting Started

This repo will allow you to get the codebase to build a new Gatsby website which has been configured to pull its content from Drupal. Both Gatsby and Drupal run locally.

### Requirements

#### Operating System:

* macOS 10.13 or later
* Windows 10 Pro+ or equivalent \(eg Windows 10 Enterprise\) with Hyper-V running
* Linux with kernel version 4.x or higher

#### Software:

* Docker - [macOS](https://docs.docker.com/docker-for-mac/install/) or [Windows 10](https://docs.docker.com/docker-for-windows/install/)
* Lando - [macOs](https://docs.lando.dev/basics/installation.html#macos) or [Windows 10](https://medium.com/@jiles/installing-lando-docker-and-composer-on-a-windows-10-pro-environment-e405efba2c96)
* NVM
* NodeJS & NPM

**Instructions for installing NVM, Node & NPM on** [macOS](https://medium.com/@jamesauble/install-nvm-on-mac-with-brew-adb921fb92cc) or [Windows](https://codeburst.io/nvm-for-windows-how-to-install-and-use-13b7a4209791).

## 1. Clone the repo

You can clone or download the repo anywhere in your computer \(i.e. Sites, Downloads, Documents, Desktop, etc.\)

```text
git clone git@github.com:mariohernandez/gatsby_training.git
```

## 2. Build the environments:

* After cloning the repo, cd into the newly created directory:

**NOTE**: _This is the default directory generated by cloning the repo. If you changed the directory name when cloning the repo, cd into that directory instead_.

```text
cd gatsby_training
```

#### Start Lando

```text
lando start
```

_This will build your Docker containers needed to run Gatsby and Drupal. **NOTE**: Docker needs to be running before running `lando start`._

#### _Start Gatsby_

_Since Gatsby pulls data from Drupal, Drupal needs to be running by completing the previous step first._

```text
cd gatsby
```

```text
nvm use
```

_If you get errors, you can try running:_ `nvm install` then `nvm use`. _This will use the version of node specified inside `.nvmrc`_

```text
npm install
```

_This will install all of Gatsby/node dependencies_.

```text
gatsby develop
```

_This will start Gatsby which should immediately connect to Drupal to pull all content_.

## 3. Access your Gatsby and Drupal sites

#### Gatsby:

[http://localhost:8000/](http://localhost:8000/)

#### GraphQL

[http://localhost:8000/\_\_\_graphql](http://localhost:8000/___graphql)

#### Drupal:

[https://nitflex.lndo.site](https://nitflex.lndo.site)

### Login to Drupal: \(switch to http if https is not working\)

[https://nitflex.lndo.site/user/login](https://nitflex.lndo.site/user/login)

Your credentials are: username: `admin`, password: `admin`
