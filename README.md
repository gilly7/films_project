# films_project

A simple app to manage information about films and its genres.
A totally functional CRUD (Create-Read-Update-Delete) application with Django by using one of its most powerful features: the Class-based Views (CBV). 


## How to Install the Project
<br />
1. You need to have Python installed in your machine (3.8 or higher is recommended);

2. Create a new folder in your machine, go inside it and clone this repository. 

3. Create a virtual environment with `venv`. I called mine `.myenv`, but you can choose another name you prefer:

<span style="margin-left: 25px;">```python -m venv .myenv```</span> 

4. Activate the virtual environment. Below is the command for most Linux OS:

<span style="margin-left: 25px;">```source .myenv/bin/activate```</span>

<span style="margin-left: 25px;">Check this [Python documentation page](https://docs.python.org/3/library/venv.html) if you have doubts about the command to start your virtual environment.</span>

5. Install the required Python modules (`django` and `django-extensions`):

<span style="margin-left: 25px;">```pip install -r requirements.txt```</span>

> **IMPORTANT NOTE**: The file `settings.py` is using a secret key setup with the `configparser` builtin Python module. So:

6. Change the name of `config_file_starter.ini` to `config_file.ini`

7. activate the Django shell:

<span style="margin-left: 25px;">```python manage.py shell```</span>

8. In the Django shell, execute the following code to generate a new secret key for your project:

<span style="margin-left: 25px;">```from django.core.management.utils import get_random_secret_key```</span>
<span style="margin-left: 25px;">```print(get_random_secret_key())```</span>


9. Copy the new secret key and paste it inside your `config_file.ini` file, replacing the `PutYourSecretKeyHereWithoutQuotationMarks` information. Don't use quotation marks here.

10. Run `python manage.py makemigrations` and `python manage.py migrate` to create the necessary tables in the database; 

11. If you want your films app to be populated with a list of Pixar movies, you can also run this command:

<span style="margin-left: 25px;">```python manage.py runscript load_pixar```</span>

<br />

## How to Use the Project
<br /> 

1. Start the local server with `python manage.py runserver`. 8000 is the default port used by Django;

2. On your browser, access the address http://localhost:8000;

3. Explore the Films CRUD funcionalities: 

* list all films;
* list details from one film;
* create a new film; 
* update and delete a film.

<br />
## Licence
<br />

This project is distributed under the MIT licence (see the LICENCE document).

Inspired by this [article](https://towardsdatascience.com/build-a-django-crud-app-by-using-class-based-views-12bc69d36ab6)
