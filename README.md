# Sample Docker environment to start any Django project.
- This is the first configuration files for start a Django project with Docker.

## Guide
Step 1: Clone this repository.

	$ git clone
	
Step 2: Create your Django project with Docker support.

	$ cd <project_root_dir>
	$ docker-compose run web django-admin startproject <your_project_name> .
	$ sudo chown -R $USER:$USER .
		
Step 3: Connect the database. 
	- Add config database for your Django project:
	// <your_project_name>/settings.py  
	
	```javascript
	DATABASES = {
	    'default': {
	        'ENGINE': 'django.db.backends.postgresql',
	        'NAME': 'postgres',
	        'USER': 'postgres',
	        'HOST': 'db',
	        'PORT': 5432,
	    }
	}
	```

Step 4: Start project with docker.

	$ cd <project_root_dir>
	$ docker-compose up

Step 5: Finish. 
	Open your browser: <a href="http:127.0.0.1:8000" target="_blank">http:127.0.0.1:8000</a>
