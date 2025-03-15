# Utiliser l'image officielle de Python
FROM python:3.8-buster

# Mainteneur de l'image
LABEL maintainer="Omar Louis Kao"

# Définir le répertoire de travail
WORKDIR /

# Copier les fichiers nécessaires dans le conteneur
COPY student_age.py /student_age.py
COPY student_age.json /data/student_age.json
COPY requirements.txt /requirements.txt

# Installer les dépendances
RUN apt update -y && apt install -y \
    python-dev python3-dev libsasl2-dev libldap2-dev libssl-dev && \
    pip3 install -r /requirements.txt

# Exposer le port de l'API
EXPOSE 5000

# Définir le point d'entrée
CMD ["python3", "/student_age.py"]
