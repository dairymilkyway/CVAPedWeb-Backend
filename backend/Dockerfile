# Use official Python 3.11 slim image
FROM python:3.11-slim

# Set the working directory inside the container
WORKDIR /app

# Copy requirements first (so Docker can cache this layer)
COPY requirements.txt .

# Upgrade pip and install dependencies
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the backend code
COPY . .

# Expose the port your app uses
EXPOSE 5000

# Set the command to run your app
CMD ["python", "app.py"]