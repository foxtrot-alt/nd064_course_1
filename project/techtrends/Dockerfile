FROM python:3.8

WORKDIR /usr/src/app

# Copy the requirements.txt file to the working directory
COPY requirements.txt ./

# Install the dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy all the files from the current directory (where the Dockerfile is located) to the container's working directory
COPY . .

# Initialize the database
RUN python init_db.py

# Expose the port the application runs on
EXPOSE 3111

# Run the application
CMD [ "python", "app.py" ]
