
## Requirements
------------------
- Python 3.6
- Django 3.1
- Django REST Framework

## Installation
------------------
After you cloned the repository, you want to create a virtual environment, so you have a clean python installation.
You can do this by running the command
```
python -m venv env
```

After this, it is necessary to activate the virtual environment, you can get more information about this [here](https://docs.python.org/3/tutorial/venv.html)

```
source env/bin/activate
```

You can install all the required dependencies by running
```
pip install -r requirements.txt
```

## Structure
-----------------
In a RESTful API, endpoints (URLs) define the structure of the API and how end users access data from our application using the HTTP methods - GET, POST, PUT, DELETE. Endpoints should be logically organized around _collections_ and _elements_, both of which are resources.

In our case, we have one single resource, `movies`, so we will use the following URLS - `/movies/` and `/movies/<id>` for collections and elements, respectively:

Endpoint |HTTP Method | CRUD Method | Result
-- | -- |-- |--
`movies` | GET | READ | Get all movies
`movies/:id` | GET | READ | Get a single movie
`movies`| POST | CREATE | Create a new movie
`movies/:id` | PUT | UPDATE | Update a movie
`movies/:id` | DELETE | DELETE | Delete a movie

## Use
-------------------
Install Httpie:

Use the command pip install httpie to install Httpie. Httpie is a user-friendly HTTP client written in Python that simplifies making HTTP requests.
Run Django Migrations:

Execute the commands python manage.py makemigrations and python manage.py migrate to apply migrations and set up the database for the Django project. This ensures that the necessary tables are created.
Add Movie Details:

Use the Django shell by running python manage.py shell.
Import the Movie model and the User model.
Create an instance of the Movie model with details like title, genre, year, and creator (associated with a user).
Save the movie instance to add entries to the SQLite database.
Start Django Development Server:

Begin the Django development server with the command python manage.py runserver. This allows you to view and interact with the Django project locally.
Attempt API Access Without Authentication:

Try accessing the API using Httpie without providing authentication credentials. This should result in an error message indicating that authentication credentials were not provided.
Access API with Valid Credentials:

Use Httpie to make a request to the API with valid authentication credentials. The provided example includes an access token in the Authorization header. This allows access to the API services.
View All Movies and Specific Movie:

Upon successful authentication, access the API endpoint to retrieve information about all movies (http://127.0.0.1:8000/api/v1/movies/).
Optionally, access information about a specific movie by providing its ID (http://127.0.0.1:8000/api/v1/movies/1/).


