FROM python:3.10-slim-buster

# Inside the container a new folder
WORKDIR /backend-flask

# From the outside copy to inside the container.
COPY requirements.txt requirements.txt

# Inside the container install the python libraries.
RUN pip3 install -r requirements.txt

# . means everything in the current directory.
# Copy everything from /backend-flak (outside) to /backend-flask (inside)
COPY . .

# Setting environment variables inside the container.
ENV FLASK_ENV=development

EXPOSE ${PORT}


CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]