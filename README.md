# Steps to install.

To get my laptop ready for deployment, I used the tools pointed out below.

LocalTunnel is a tool that allows me to set my localhost as a ip public.

### Tools: 
1. Docker desktop
2. Rocket.chat environment
3. LocalTunnel
   

## Installation
___
### 1 _ Docker Desktop:

Go to https://docs.docker.com/desktop/install/windows-install/, download and install.

---
### 2 _ Rocket.chat environment:

1. Download and install: WSl 2 - Install Linux on Windows with WSL.
2. Download and install the latest Linux Kernel Updates.
3. Download and install:: NodeJS.
4. Install Meteor.

---
### 3_ LocalTunnel:
1. run on WSL 2: npm install -g localtunnel
___





# Rocket.chat API Test

Searching the Rest API documentation on rocket.chat.com, we have all the necessary documentation to run these queries.

As the documentation points out, authentication is required for any query/update. For this, I created in the header the X-Auth-Token and X-User-Id, which are generated in the Token access tool on Rocket.chat workspace.

---

### 1 _ Create a new user via an API endpoint
---
To create a new user, do you need to send a post request on postman,

Method: POST.

- run: localhost:3000/v1/api/users.create

Required Argument:
{name:,
email:,
password:,
username:,}

Fill the required data and then do you *create a user*.

---
### 2 _ Get the room information via an API endpoint
---

To be able to get the room information do you have to create a group.

Creating a group you will generate an Id.

To create a group do you need to run this command on postman:

Method: GET.

- localhost:3000/api/v1/groups.create

Required argument ->
{name:}

*Then you generate an id, using this id we will be able to get the room info.*

TO GET THE ROOM INFORMATION:

- Run -> localhost:3000/api/v1/rooms.info

Required argument:
roomId: Id do you generate when create a group.

Done.

You get the room information.

---
### 3 _ Get a list of all user roles in the system via an API endpoin
---
Method: GET

To get all the users roles do you need to run a get command on postman:

 - run: http://localhost:3000/api/v1/roles.list

And done do you have all the roles a user can be.