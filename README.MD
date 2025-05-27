// You only need docker-compose.yml file for deployment.

// Everything is included in the docker images used by docker-compose.

// Most settings are set vie environment vairbales through docker-compose.

// Compatible only with Linux amd64 - Windows (WSL2.0)

################

Project Overview

################

This Python (Django) project contains 2 Main Apps:

	1.	User App - A complete comprehensive user management system allowing staff members to add, edit, and manage user permissions, a profile page for users to view and update their details.

	2.	Documents App - A robust complete app for managing Ministry Decrees, and other related documents. The app includes secondary sections which are Countries, Document Types, Governments, and Decree Catagories, all of which interconnected with foreign key relationships to the main models. In addition to open viewership to the public.

Technologies Used

#################

  •	Docker Compose [Containerization]:
	
	  •	Application Service [linux debian]:
		
			Backend Framework [Python 3.13]:
			
			  •	Django 5.1.7 (Main Server Framework)
			
			  •	gunicorn 23.0.0 (Main WSGI Server)
			
			  •	django-tables2 2.7.1 (Table Views)
			
			  •	django-crispy-forms 2.3.0 (Forms Rendering)
			
			  •	django-filter 24.3 (Query Filters)
			
			  •	celery[redis] 5.4.0[5.2.1] (Tasks)
			
			  •	django-redis 5.4.0 (django redis adapter)
			
			  •	django-celery-beat 2.7.0 (django celery adapter)
			
			  •	psycopg2-binary 2.9.10  (PostgreSQL database adapter)
			
			  •	Plotly (Interactive charts)
		
			Frontend Components:
			
			  •	Django 5.1.7 (Main Server Framework)
			
			  •	Html + CSS + Javascript (With Django Templates)
			
			  •	Bootstrap5 (Main Visual Framework)
			
			  •	jQuery (Javascript for Autocomplete)
			
			  •	AJAX (Real-time Requests to Server)
			
			  •	Flatpickr (Date Picker)
	
		Database Services:
		
		  •	PostgresSQL 17 (Main Database)
		
		  •	PostgresSQL 17 (Backup Database)
	
		Redis Service:
		
		  •	Redis server 7 (Cache Server)
	
		Migrator Service:
		
		  •	Application Service Image (Makes and Admits New Migrations to Database)
	
		Celery Service:
		
		  •	Celery 5.4.0 (Background Tasks Server)
	
		pgAdmin Service:
		
		  •	pgAdmin 4 (Database Admin Interface)
	
		nginX Service:
		
		  •	nginx (Static and Media Server)

Version History

###############

v0.1.0 - Initial Deployment

	•	Initialization of django project with initial requirements, a dockerfile, and an initial commit of the project to git.


v0.1.5 - First Development Update

	•	Basic structure for the main app established with models for Decrees, and secondary sections.

	•	Django-tables2, django-crispy-forms, and django-filter were added to the backend.

	•	Bootstrap 5, flatpickr, and Plotly.js added for the frontend design.

	•	Basic view for Decrees added, with pagination, tables, forms, and filters for the Decree model.

	•	Reused The user app from Trademarks Project with a few tweaks and changes.


v0.1.11 - Second Development Update

	•	Reused advanced search features from the Trademarks project with a few adjustments.

	•	Added Minister forms and filters, and added an AJAX function for improved selections.

	•	Improved Minister and Government reltions in forms, filters, and in the tables, in addition to their relation to decrees.

	•	Reused the Report function from Trademarks project with a few adjustments and improvements.

	•	Implemented the downloader and excel_export functions from Trademarks project with a few tweaks.

	•	Switched to Category based tab separation in decree table view instead of status.


v0.1.13 - Third Development Update

	•	Finished the Decree Reports section to be based on minister, government, and year with dynamic dropdown menus.

	•	Reworked the index page to include latest entries and be more specific to Decree model.


v0.2.1 - Stable Release Update

	•	Implemented a management command to import old data to db and edited xlsx files to avoid errors during import.

	•	Introduced a User based field to the min model for created_by and updated_by.