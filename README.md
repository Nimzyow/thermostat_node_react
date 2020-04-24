# Thermostat with Node, Express and React

This was a passion project inspired by a Makers Academy Thermostat challenge done with Jquery, Javascript, HTML and Sinatra.

I decided to challenge myself by completing this challenge with Node.js and Express.js for the backend and React for the front end. React components use hooks and functional components to keep code as clean as possible. Testing was done with Cypress, jest and enzyme.

## Table of content

- [Installation](#installation)
- [Creating the database](#creating-the-database)
- [Testing](#testing)
- [Running the project](#running-the-project)
- [Tech stack](#tech-stack)

## Installation

Follow these steps to install required dependencies:

1) on root of project run:

```
$ npm install
```

2) cd one directory into thermostat and again run:

```
$ npm install
```

## Creating the database

Right, so you will need to setup up the database before running this app, but there is a pre-requisite. You will need to make sure you have sqlite installed in your system. If you don't, please visit https://www.sqlite.org/download.html and download the right version for your system.

When installed, create a directory anywhere you want to store your database.

When installation is done, cd into the folder which you intend to have your database in. Once there, run:

```
$ sqlite3 thermostat
```

sqlite will be running. Create the following table:

```
CREATE TABLE thermo(temperature, city);
```

if successful, you should be able to run the following and see the structure of your thermo table:

```
$ .schema thermo
```

Once successful, you will need to open db.js, conveniently located in the root of this project, and change the storage location:

```
const sequelize = new Sequelize({
  dialect: "sqlite",
  storage: "PATH_FROM_ROOT_OF_YOUR_COMPUTER_TO_DATABASE_LOCATION"
});
```

And that's it for setting up the database! Phew!!

## Testing

For Jest and Enzyme tests:
cd into thermostat and run:

```
$ npm test
```

For Cypress Tests:
Stay in the thermostat directory or cd into it if you have not done so already and run:

```
$ npm run cypress
```

## Running the project

You will need to start the server. So in the root of the project run:

```
$ node index.js
```

cd into thermostat and run:

```
$ npm start
```

Enjoy :)

## Tech stack

- JavaScript
- React
- Node
- Express
- Cypress
- Jest and Enzyme
- Hooks

