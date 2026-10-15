# Prueba cruzada del proyecto

## 1. Información general

- **Proyecto:** Gestor de Tareas Full Stack con Docker.
- **Fecha de la prueba:** 14 de octubre de 2026.
- **Persona que realizó la prueba:** Eleanyeris Hernandez.
- **Tipo de prueba:** Prueba cruzada en un computador diferente al utilizado para el desarrollo.
- **Repositorio:** https://github.com/gpsanchezr/fullstack-docker-task-manager

## 2. Objetivo

Comprobar que el proyecto puede descargarse desde GitHub, configurarse y ejecutarse en un computador diferente al utilizado para el desarrollo, siguiendo las instrucciones del archivo `README.md`.

## 3. Procedimiento realizado

La compañera Eleanyeris Hernandez clonó el repositorio directamente desde GitHub y realizó los siguientes pasos en el computador de prueba:

1. Clonó el repositorio:

   ```powershell
   git clone https://github.com/gpsanchezr/fullstack-docker-task-manager.git
   ```

2. Ingresó a la carpeta del proyecto:

   ```powershell
   cd fullstack-docker-task-manager
   ```

3. Creó el archivo de configuración local a partir de la plantilla:

   ```powershell
   Copy-Item .env.example .env
   ```

4. Configuró las variables necesarias en el archivo `.env`.

5. Construyó las imágenes e inició los servicios:

   ```powershell
   docker compose up -d --build
   ```

6. Consultó el estado de los contenedores:

   ```powershell
   docker compose ps
   ```

7. Abrió la aplicación en el navegador:

   http://localhost:8080

## 4. Resultados observados

De acuerdo con la prueba cruzada y la evidencia registrada:

- Se ejecutó el proceso de construcción e inicio de los servicios Docker en el segundo computador.
- Se observaron los contenedores correspondientes a la base de datos (`bd`), la API (`api`) y el frontend (`frontend`).
- Se abrió la interfaz web mediante `http://localhost:8080`.
- Se observaron en la aplicación las siguientes tareas:
  - Clonar repositorio de GitHub.
  - Levantar contenedores Docker.
  - Redactar archivo de prueba cruzada.

Estos resultados respaldan la reproducción del despliegue en un equipo diferente al de desarrollo. No se consideran verificadas otras operaciones, como completar o eliminar tareas, ni la persistencia de los datos después de recrear los contenedores, porque no forman parte de los resultados aquí documentados.

## 5. Evidencia

La captura de pantalla de la prueba cruzada debe conservarse en la siguiente ruta del repositorio:

`evidencias/fase6-prueba-cruzada.jpg`

La imagen debe corresponder a la prueba realizada y mostrar, según la evidencia disponible, el estado de los contenedores y la aplicación abierta en el navegador.

## 6. Conclusión

La prueba cruzada realizada por Eleanyeris Hernandez permitió comprobar que el repositorio puede clonarse desde GitHub, que los servicios Docker pueden iniciarse en un computador diferente y que la interfaz web puede abrirse siguiendo el procedimiento documentado.

Los resultados constituyen evidencia de la reproducibilidad básica del despliegue y permiten identificar posibles mejoras en las instrucciones del README. La conclusión se limita a los pasos y resultados efectivamente observados durante la prueba.

