# BikeStoreETLProject

Pipeline ETL con arquitectura Medallión usando Databricks y visualización con Matplotlib. Proyecto de ingeniería de datos con el dataset "Bike Store Relacional".

- [Aruitectura del proyecto ETL con Databricks](Docs/Arquitectura_Pipeline.png)

## Descripción
Este proyecto implementa un pipeline ETL completo en Databricks Community Edition, siguiendo la arquitectura Medallión (Bronze, Silver, Gold). El objetivo es procesar el dataset "Bike Store Relacional" para generar tablas analíticas, visualizar los datos con gráficos, y extraer conclusiones accionables. Incluye:

- **Extracción**: Ingestión de datos crudos a la capa Bronze.
- **Transformación**: Limpieza y estandarización en la capa Silver.
- **Carga**: Creación de tablas analíticas en la capa Gold (ventas por tienda, productos más vendidos, análisis de clientes).
- **Orquestación**: Ejecución del pipeline con un notebook maestro.
- **Visualización**: Gráficos generados con Matplotlib.
- **Análisis**: Conclusiones basadas en los datos visualizados.

## Estructura del Repositorio
- `notebooks_dbc/`: Notebooks de Databricks en formato `.dbc` (`Extract.dbc`, `Transform.dbc`, `Load.dbc`, `PipelineOrchestrator.dbc`).
- `notebooks_html/`: Versiones HTML de los notebooks para visualización directa (`Extract.html`, `Transform.html`, `Load.html`, `PipelineOrchestrator.html`).
- `docs/`: Documentación del proyecto en PDF (`BikeStoreETLDocumentation.pdf`).
- `presentation/`: Presentación en PDF (`BikeStoreETLPresentation.pdf`).

## Visualización de los Notebooks
- Los notebooks están disponibles en formato `.dbc` en la carpeta `notebooks_dbc/`. Para verlos, importa los archivos a Databricks:
  1. Ve a tu Workspace en Databricks.
  2. Haz clic en "Import".
  3. Selecciona el archivo `.dbc` y súbelo.
- También puedes ver una versión estática de los notebooks en formato HTML en la carpeta `notebooks_html/`. Descarga los archivos `.html` y ábrelos en tu navegador.

## Dataset
El dataset "Bike Store Relacional" proviene de Kaggle: [Bike Store Dataset](https://www.kaggle.com/datasets/dillonmyrick/bike-store-sample-database). Incluye tablas como `orders`, `products`, `customers`, y `stores`.

## Resultados
- **Ventas por tienda**: Baldwin Bikes lidera con más de 5M en ventas.
- **Productos más vendidos**: La marca Electra domina, con el Surly Ice Cream Truck Frameset como el producto estrella.
- **Análisis de clientes**: Identificación de clientes de alto valor (hasta 35,000 dólares en gastos).

## Conclusiones
- Replicar las estrategias de Baldwin Bikes en otras tiendas.
- Promocionar más productos de la marca Electra.
- Implementar programas de fidelización para clientes de alto valor.

## Herramientas Utilizadas
- **Databricks Community Edition**: Para el pipeline ETL.
- **PySpark**: Para procesamiento de datos.
- **Matplotlib**: Para visualización.
- **Notion**: Para documentación.
- **PowerPoint**: Para la presentación.

## Instrucciones para Reproducir
1. Configura un clúster en Databricks Community Edition.
2. Sube los archivos CSV del dataset a `dbfs:/FileStore/bike_store_data/landing/`.
3. Importa los notebooks `.dbc` a Databricks y ejecuta `PipelineOrchestrator.dbc` para correr el pipeline completo.
4. Revisa los gráficos y análisis en `Load.dbc`.

## Licencia
Este proyecto está bajo la licencia MIT. Siéntete libre de usarlo y modificarlo.

## Contacto
Conéctate conmigo en [LinkedIn](www.linkedin.com/in/erickson-otaño>) para más proyectos de datos.
