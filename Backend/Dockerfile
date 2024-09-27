# Use the official Python image
FROM python:3.11-slim

# Set the working directory in the container
WORKDIR /app

# Copy requirements.txt and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the entire content of the Backend folder
COPY . .

# Command to run the application
CMD ["gunicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]
