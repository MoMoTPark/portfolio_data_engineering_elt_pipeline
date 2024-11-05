### Portfolio - data engineering ELT pipeline demo project

#### Project summary

This is a demo project with the aim to demonstrate a extract, load, transform (ELT) pipeline utilising a toy dataset with an automated data retrieval script implemented in Python using Docker containers and PostgreSQL. 

#### Project contents

Docker Desktop is required to run this demo.

This pipeline is fully managed in a network of Docker containers with dedicated volume management for data persistence in the following structure:

- Source PostgreSQL which is the first service specified in `compose.yaml`. This database is initialized with demo data to be deposited onto the destination database. 
- Destination PostgreSQL database which is specified as the second service in `compose.yaml`.
- An image instance built to run `elt_script.py` based on the provided `Dockerfile`.
- a network to allow communication between containers.

#### Associated technical skills and technologies

- SQL (PostgreSQL)
- Python
- Docker
- Bash