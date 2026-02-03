# connectatel-analisis-de-uso-y-segmentacion-de-clientes-latam
Objetivo del Proyecto
  El objetivo de este proyecto es analizar el comportamiento real de uso de los clientes de ConnectaTel (llamadas y mensajes) para:
    identificar patrones de consumo,
    detectar comportamientos atípicos (outliers),
    segmentar clientes por edad y nivel de uso,
    y generar recomendaciones accionables que ayuden a optimizar la oferta de planes y mejorar la experiencia del usuario.

  El análisis se realiza con datos históricos hasta el año 2024.

Datasets Utilizados
  El proyecto se basa en tres fuentes de datos que se complementan entre sí:
    plans.csv =>	Catálogo de planes: precio, minutos incluidos, GB incluidos y costos extra.
    users_latam.csv =>	Información de clientes: edad, ciudad, fecha de registro y plan contratado.
    usage.csv	=> Uso real del servicio: llamadas y mensajes (tipo, duración y longitud).
    
Etapas del Análisis Realizadas
  Carga y exploración inicial
    Revisión de estructura, tipos de datos y dimensiones de cada dataset.
  Identificación de problemas de calidad
    Detección de sentinels (-999, "?").
    Análisis de valores nulos y validación de nulos estructurales (MAR).
  Limpieza de datos
    Corrección de sentinels.
    Marcado de valores inválidos como NA.
    Validación de fechas fuera de rango.
  Feature engineering
    Agregación del uso por usuario:
      cantidad de mensajes,
      cantidad de llamadas,
      minutos totales de llamada.
    Construcción del perfil de usuario (user_profile).
  Análisis exploratorio
    Estadísticas descriptivas.
    Histogramas y boxplots para analizar distribuciones y dispersión.
    Detección de outliers con el método IQR.
  Segmentación de clientes
    Segmentación por nivel de uso (Bajo, Medio, Alto).
    Segmentación por edad (Joven, Adulto, Adulto Mayor).
    Visualización de la distribución de segmentos.
  Insights ejecutivos
    Identificación de segmentos de alto valor.
    Interpretación de patrones de uso extremo.
    Recomendaciones de negocio basadas en datos.

Cómo Ejecutar el Notebook
  Opción 1: Google Colab (recomendado)
    Sube este repositorio a tu cuenta de GitHub.
    Abre Google Colab.
    Selecciona File → Open Notebook → GitHub.
    Pega la URL del repositorio y abre el notebook.
    Asegúrate de subir los archivos CSV en la carpeta /datasets.

  Opción 2: Ejecución local
    Clona el repositorio:
      git clone <url-del-repositorio>
  Abre el notebook con Jupyter:
      jupyter notebook
  Ejecuta las celdas en orden.

Guía de Reproducción
  Para reproducir el análisis correctamente:
    Verifica que los archivos CSV estén en la carpeta /datasets.
    Ejecuta el notebook de arriba hacia abajo, sin saltar celdas.
    No modifiques el orden de las etapas (limpieza → agregación → análisis).
    Los gráficos y segmentaciones se generan automáticamente.

Herramientas Utilizadas
  Python
  Pandas
  NumPy
  Seaborn
  Matplotlib
  Jupyter Notebook

Conclusión
  Este proyecto muestra un flujo completo de análisis de datos aplicado al negocio, desde la limpieza y validación hasta la segmentación y generación de insights, listo para revisión técnica o presentación a     stakeholders.
