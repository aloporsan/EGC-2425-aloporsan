# Usar una imagen base de Python
FROM ubuntu:latest

# Establecer el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copiar el archivo de requisitos al directorio de trabajo del contenedor
COPY requirements.txt .

RUN apt-get update && apt-get install -y curl
RUN apt-get install -y net-tools iputils-ping

# Copiar el contenido de tu aplicación al directorio de trabajo del contenedor
COPY . .

# Exponer el puerto que usa Flask
EXPOSE 5000

# Comando para ejecutar la aplicación Flask
CMD ["python", "app.py"]