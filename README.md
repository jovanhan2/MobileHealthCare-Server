
# About
* Utilises Socket IO with websockets (NodeJS + Javascript)
* Can be hosted locally or on the cloud
* Uses SQLITE3 to store data 
* npm for dependencies 
# To Start
* Run `npm install in the root folder`
* If any errors (usually on Windows) run `npm install --vs2015 -g windows-build-tools`
* Run `npm start` to start the server 
* The server should be started at `localhost:65080`
* Local host is your current ip address
* Be sure to use HTTP instead of HTTPS

Our cloud server implementation is identicial, except that it is running on a Google Cloud VM instance
* 35.246.29.217:65080/ (most likely not running now)



# Responsibilities of the server 
* Save relevant data to SQL database (resources/storage.db)
* Respond to query from app/raspberry PI to database (e.g. medication details)
* Process the pillbox state machine to determine which pill to open next


# Pill
* Get times for next pill 
* When time reaches, emit indicator to pillbox as to which box to open next
* Once pill is taken record time taken

# Example object

* Saving user details to the SQL database
* Send this JSOn object over SocketIO to the server

```js
{
  type: "userDetails",
  data: {
    Username: "testUser",
    Password: "testPassword",
  }
}
```

