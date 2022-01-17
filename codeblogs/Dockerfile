FROM python

WORKDIR /app

#upgrading pip for python
RUN python3 -m pip install --upgrade pip

#copy the requirement.txt file for downloading all the required dependencies
COPY ./requirements.txt .

#install those requirements before copying the project
RUN pip install -r /app/requirements.txt

#copy the project
COPY . .

#run gunicorn. here codeblogs is the project name
CMD gunicorn -b 0.0.0.0:$PORT codeblogs.wsgi:application




