

# To Start

### 1 - Create Project

	docker-compose run web django-admin.py startproject trymeproject .


### 2 - Configure Database


Change in *trymeproject/settings.py* : 

	DATABASES = {
	    'default': {
    	    'ENGINE': 'django.db.backends.postgresql_psycopg2',
        	'NAME': 'postgres',
	        'USER': 'postgres',
    	    'HOST': 'db',
        	'PORT': 5432,
	    }
	}


### 3 - Run docker-compose up

	docker-compose up
	
Or to background mode:

	docker-compose up -d	
	
### 4 - Running tests

	docker-compose run web python manage.py test
	
### 5 - View on Browser

	localhost:8000		


# References 

* [Getting started with Docker and Django](https://howchoo.com/g/y2y1mtkznda/getting-started-with-docker-compose-and-django)