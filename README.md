# Cinema API

**DRF** project where implemented basic api logic for creating movies with genres and actors, movie sessions, 
and orders with tickets for this movie sessions. 
<br/>
`PosgtreSQL` used as DB and `Docker` with docker-compose for DB and API

## Prerequisites
> 👉 You should have Docker installed on your local machine [link](https://www.docker.com)

## Installing instructions
> 👉 Clone this repository  

```bash
$ git clone git@github.com:kuznetsb/cinema-api.git
```
<br />

> 👉 Configure environmental variables
```bash
$ create .env file in project directory
$ Use .env.sample as template and copy all those DB variables to .env
$ fill DB variables with your values in .env file (exmaple: POSTGRES_DB=app)
```
Now your Postgres database will be configured properly

<br />

> 👉 Run docker-compose

```bash
$ docker-compose up
```
That will application with all installed dependencies, database and so on.
Now you can use API!
<br />
<br />

## Usage instructions

> 👉 At this point, the app runs at http://127.0.0.1:8000/
<br />
👉 Go to /api/doc/swagger/ to see documentation with endpoints
```bash
$ /api/user/register/ to create new user
$ /api/user/token/ to authorize after creating and get token
$ /api/user/token/reftesh/ to refresh access token when it goes out of time
```
<br />

> 👉 Note: API has ReadOnly restrictions for non-staff users
> <br />
> If you want to try all functionality follow next steps:
```bash
$ run docker exec -it <container_id> sh in terminal
$ run python manage.py createsuperuser and follow next steps
```
Now you can use staff user, just do 2 and 3 steps from instruction for non-staff user

## Features
* JWT authenticated
* Admin panel /admin/
* Documentation is located at /api/doc/swagger/
* Managing orders and tickets
* Creating movies with genres, actors
* Creating cinema halls
* Adding movie sessions
* Filtering movies and movie sessions