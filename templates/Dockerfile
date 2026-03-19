FROM python:3.7-slim
WORKDIR /app
RUN  pip install pipenv 
COPY Pipfile Pipfile.lock ./

RUN pipenv install --system --deploy 
COPY  . .
EXPOSE 5000
CMD [ "flask", "run", "--host=0.0.0.0" ]
