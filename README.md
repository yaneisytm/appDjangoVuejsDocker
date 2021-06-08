# appDjangoVuejsDocker
Pasos a seguir:


# Construir la imagen de backend 
docker build --tag=backend .

# Construir la imagen de frontend
docker build --tag=frontend .

# Iniciar sesion
docker login

# subir las imagenes a dockerhub etiquetadas  
 docker image tag backend yaneisy/backend:django
 docker image tag frontend yaneisy/frontend:vue-js

 docker image push  yaneisy/backend:django
 docker image push  yaneisy/frontend:vue-js


# levantar ambos servicios webs 
docker-compose up


 # url a ver  en la web 
 http://35.239.81.26:8080 --> frontend
 http://35.239.81.26:8000 -->  backend


