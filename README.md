# bearer-auth

## Authentication Server Phase 2: Token (Bearer) Authentication

* At this point, our `auth-server` is able to allow a user to create an account as well as to handle Basic Authentication (user provides a username + password). When a “good” login happens, the user is considered to be “authenticated” and our auth-server generates a JWT signed “Token” which is returned to the application

## Phase 2 Requirements

* In this phase, the new requirement is that any user that has successfully logged in using basic authentication (username and password) is able to continuously authenticate … using a “token”

* As a user, I want to obtain a token after I signin, so that I can re-authenticate

  * Using an HTTP REST client, or a web form:

        * Following a POST to `/signup` to create an account (or) Following a POST to `/signin` with basic authorization

        * Send a response to the client with the proper status code along with an object with the following properties 

          {
            user: {
              _id: 'ID FROM DB',
              username: 'myusername'
            },
            token: 'JWT Token Here'
          }

## Links

* [Heroku]()

* [Bearer-auth Repo](https://github.com/SdMartinez13/bearer-auth)