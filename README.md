# Backend
#### Production branch deployed at https://limitless-earth-34461.herokuapp.com/
##### Seeded information can be accessed by logging in with the following credentials
```
username: test1
password: password
```

# Endpoints

#### Login/Register Routes

| Method | Endpoint                |  Description                                  |
| ------ | ----------------------- |  -------------------------------------------- |
| POST   | `/api/auth/login`       |  Logs in and returns token                    |
| POST   | `/api/auth/register`    |  Creates a new user                           |


#### User Routes
These endpoints are protected, you will need to be logged in to access them.

| Method | Endpoint                 |  Description                                                                         |
| ------ | ------------------------ |  ----------------------------------------------------------------------------------- |
| GET    | `/api/user`              |  Returns current user logged in               |
| PUT    | `/api/user/:id`          |  Edits user with the matching id              |
| DELETE | `/api/user/:id`          |  Deletes user with the matching id            |

#### Plant Routes
These endpoints are protected, you will need to be logged in to access them.

| Method | Endpoint                     |  Description                                                                       |
| ------ | -----------------------      |  --------------------------------------------------------------------------------- |
| GET    | `/api/plants`              |  Returns plants belonging to current user |
| GET    | `/api/plants/:id`          |  Returns info for specific plant          |
| POST   | `/api/plants`              |  Creates a new plant                      |
| PUT    | `/api/plants/:id`          |  Edits plant by id                        |
| DELETE | `/api/plants/:id`          |  Deletes the plant by id                  |

# Data Schema

#### Users
```js
{
    username:     STRING     // required
    password:     STRING     // required
    phone_number: STRING     // required example: (999)-999-9999 or 999-999-9999
}
```
#### Plants
```js
{
    user_id:        INTEGER      // required (handled by backend)
    nickname:       STRING       // required
    species:        STRING       // required
    h2oFrequency:   STRING       // required
    image:          STRING       // optional
}
```

![alt text](https://github.com/Lambda-Build-Week-Water-My-Plants-II/back-end/blob/master/Water_My_Plants_DB_DESIGN.png "Water my plants")
