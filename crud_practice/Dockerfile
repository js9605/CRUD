# Pobierz oficjalny obraz Python
FROM python:3.11.4

# Ustaw katalog roboczy w kontenerze
WORKDIR /crud_practice

# Install system dependencies
RUN apt-get update && apt-get install -y postgresql-client

# Skopiuj pliki aplikacji do kontenera
COPY . /crud_practice

# Zainstaluj zależności z pliku requirements.txt
RUN pip install -r requirements.txt

# Odsłuchuj na porcie 8000
EXPOSE 8000

# Uruchom serwer Django
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
