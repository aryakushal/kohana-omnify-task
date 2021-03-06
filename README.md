# Kohana RESTful API

API end point for the following Signup, Login, Create User Profile (After Login), View User Profile (After Login) and Logout.

## How this shit works?
* Open up http://localhost/omnify-task/index.php/ in browser.
* Interact with the app using Postman (for Google Chrome) or RESTClient (for Firefox).
* Variables to be posted to a URI can be found by GET request to the URI.

### API details
| Action         | Path                                | Method | Accepted variables                  |
|----------------|-------------------------------------|--------|-------------------------------------|
| Sign Up        | `/index.php/v1/auth/signup`         | POST   | username, email, password           |
| Login          | `/index.php/v1/auth/login`          | POST   | email, password                     |
| Logout         | `/index.php/v1/auth/logout`         | GET    | N/A                                 |
| Create Profile | `/index.php/v1/profile/create`      | POST   | fname, lname, gender, age, location |
| View Profile   | `/index.php/v1/profile`             | GET    | N/A                                 |

### Database
`database-mysql.sql` is your database file. Following command can be used to setup the database on Linux machines.

### Installation
```
$ sudo add-apt-repository ppa:ondrej/php
$ sudo apt install apache2 php5.6 mysql-server php5.6-mysql
$ cd /var/www/html/
$ git clone https://github.com/VijayKumarHackr/kohana-omnify-task.git omnify-task
$ cd omnify-task/
$ mysql -u username -p database < database-mysql.sql
```

**NOTE**: Tested using RESTClient (for firefox).
