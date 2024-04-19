# Mapas

## Enlaces
[Generación de mapa de riqueza de especies](https://evaluacion-arboles-mesoamerica.github.io/mapas/src/visualization/generacion-mapa-riqueza-especies-plantas.html)  

## Comandos para el manejo de la imagen y del contenedor Docker

### Generación de la imagen a partir del archivo Dockerfile
```shell
# Generación de la imagen Docker a partir del archivo Dockerfile
docker build -t arboles-r-433 .
```

### Ejecución del contenedor
```shell
# Ejecución del contenedor Docker
# (el directorio local debe especificarse en la opción -v)
# (el archivo con variables de ambiente debe especificarse en la opción --env-file)
docker run -d --name arboles-r-433 \
  -p 8787:8787 \
  -v /home/mfvargas/evaluacion-arboles-mesoamerica/github/mapas:/home/rstudio \
  arboles-r-433
```
  
### Acceso al contenedor (username=rstudio, password=biodatacr)
[http://localhost:8787](http://localhost:8787)

### Detención, inicio y borrado del contenedor
```shell
# Detención del contenedor Docker
docker stop arboles-r-433

# Inicio del contenedor Docker
docker start arboles-r-433

# Borrado del contenedor Docker
docker rm arboles-r-433
```
