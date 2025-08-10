# Base NodeJs project template

`src` -> contains all the code regarding the project, and doesn't include any kind of tests

Inside the `src` folder
- `config` -> contains any configuration or any library/module setup. For eg: setting up `dotenv`
- `routes` -> contains any routes, middlewares and controllers
- `middlewares` -> contains code to intercept and then authenticate or validate the requests
- `controllers` -> like last middlewares, post them we pass data to the business layer, once business layer returns the output, we structure the API response in controllers and send the output
- `repositories` -> this folder contains all the logic using which we interact with the DB by writing queries, all the raw queries or ORM queries will go here
- `services` -> contains the business logic and interacts with repositories for data from the DB
- `utils` -> contains helper methods

## Setup the project

- Download this template from github and open it in a text editor
- In the root directory create a `.env` file and add the following variables
    ```
        PORT=port number
    ```
- Inside the `src/config` folder, create a file named as `config.json` and paste in the following code:
```
{
  "development": {
    "username": "root",
    "password": null,
    "database": "database_development",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "test": {
    "username": "root",
    "password": null,
    "database": "database_test",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "production": {
    "username": "root",
    "password": null,
    "database": "database_production",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}
```