
# Laboratorio Primer Producto de Datos - Publicando un modelo de deep learning en Heroku


> Enlace Producto de Datos: https://claseudd-tarea.herokuapp.com/

> Para realizar la implementación de este primer producto de datos, se recorrio el siguiente camino:


## Antes de empezar

- Para poder realizar este laboratorio se necesita una cuenta en [GitHub](https://www.github.com/) y [Heroku](https://www.heroku.com/). Ambas son gratuitas y les serán muy útiles en el futuro.
- Se asume que el computador de cada estudiante tiene Python y Jupyter Notebook instalados (requisitos de varios cursos anteriores del programa). Si no es el caso, recomiendo seguir algún tutorial como esta [guía para instalar Jupyter Notebook en Windows 10](https://medium.com/@kswalawage/install-python-and-jupyter-notebook-to-windows-10-64-bit-66db782e1d02).

## Instalación de librerías necesarias

### Pytorch

- Seguir las [instrucciones oficiales](https://pytorch.org/get-started/locally/) seleccionando el sistema operativo correspondiente.

### fastai [(instrucciones)](https://docs.fast.ai/install.html)
```
pip install fastai
```
Al instalar el fastai no funciono a la primera, asi que fue necesario usar la siguiente instrucción
```
pip install --no-deps fastai
```
### Flask [(instrucciones)](https://flask.palletsprojects.com/en/1.1.x/installation/)
```
pip install Flask
```
### Si se desea modificar aún más la aplicación web, se recomienda usar un [ambiente virtual](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/) (además es una muy buena práctica al momento de programar en Python)

## Construcción del Modelo de Deep Learning

- Se deben seguir las instrucciones explicadas en este [notebook](https://github.com/aastroza/clase_productodatos_2019_udd/blob/master/notebooks/ejemplo_clasificador_fastai.ipynb).

## Modificación de la aplicación web

### Poner el modelo (archivo .pkl) en la carpeta `models` 

### Cambiar los nombres de las clases

- Abrir "app.py" y buscar la variable llamada `classes` y cambiar su contenido con las clases del clasificador propio.

### Modificaciones de la Interfaz

- Modificar los archivos en los directorios `templates` y `static`.

- `index.html` maneja la parte gráfica y `main.js` el comportamiento.



## Conexión con Heroku

- El primer paso es crear una aplicación y darle un nombre.

- En "Deployment Method" escoger "Connect to Github" y seguir las instrucciones.

- Una vez que esté listo, aparecerá un link para revisar la aplicacion en el navegador, como este: https://facemask-udd.herokuapp.com/

## Imagenes

Las imagenes se cargaron de acuerdo a las instruccion del notebook, pero fue necesario realizar varias iteraciones para construir el dataset.

Luego manualmente se seleccionaron las imagenes que mas se ajustaban al problema que se queria responder en este primer producto de datos.


## Créditos

- Este producto esta basado en [aastroza/clase_productodatos_2019_udd](https://github.com/aastroza/clase_productodatos_2019_udd). 
- La construcción del modelo está basada en las clases de [Francisco Ingham y Jeremy Howard](https://github.com/fastai/course-v3/blob/master/nbs/dl1/lesson2-download.ipynb). La aplicacion web está inspirada en el trabajo de [Shankar Jha](https://github.com/shankarj67/Water-classifier-fastai).
