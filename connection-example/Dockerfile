# Establece la imagen base
FROM python:3.12.5

# Establece el directorio de trabajo en el contenedor
WORKDIR /app

# Copia el archivo de requisitos al directorio de trabajo
COPY requirements.txt .

# Instala las dependencias
RUN apt-get update
RUN apt-get install -y
RUN pip install -r requirements.txt

# Copia el código fuente al directorio de trabajo
COPY . .

# Expone el puerto 9090
EXPOSE 1234

# Configura Jupyter Notebook como el comando por defecto para ejecutar la aplicación
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=1234", "--no-browser", "--allow-root", "--NotebookApp.token=123"]