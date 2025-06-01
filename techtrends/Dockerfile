# Dockerfile for TechTrends application
# Use the official Python image from the Docker Hub
FROM python:3.8

# Set the maintainer label
LABEL maintainer="Mohamed Adel"

COPY . /app
# Set the working directory
WORKDIR /app
# Install dependencies
RUN pip install -r requirements.txt

# Initialize the database
RUN python init_db.py

# Expose the application port
EXPOSE 3111

# command to run on container start
CMD [ "python", "app.py" ]
