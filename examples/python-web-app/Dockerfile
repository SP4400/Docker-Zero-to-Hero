FROM ubuntu

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file and application code
COPY requirements.txt /app/
COPY devops /app/devops/

# Update and install Python and pip
RUN apt-get update && \
    apt-get install -y python3 python3-pip

# Install the required Python packages
RUN pip install -r /app/requirements.txt

# Set the working directory to the devops directory
WORKDIR /app/devops

# Set the entry point and default command
ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




