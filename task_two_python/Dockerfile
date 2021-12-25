FROM python:3.8

WORKDIR /simple_crud

COPY ./simple_crud /simple_crud

RUN pip install -r /simple_crud/requirements.txt

ENV SECRET_KEY trw34565w4345wy
ENV DEBUG False

RUN python manage.py migrate

CMD ["gunicorn", "--bind", "0.0.0.0:8000", "simple_crud.wsgi"]