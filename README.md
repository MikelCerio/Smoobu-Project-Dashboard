# Smoobu-Project-Dashboard
 Revenue Management & Channel Performance Dashboard 🏨📊
📌 Visión General del Proyecto
Este proyecto es una solución End-to-End de Data Analytics diseñada para resolver un problema crítico en la gestión de propiedades turísticas: la falta de visibilidad unificada y en tiempo real del rendimiento de diferentes canales de distribución (Booking.com, Airbnb, Reservas Directas).

El objetivo es extraer datos crudos de estas plataformas (vía APIs o exportaciones de un Channel Manager como Smoobu), anonimizarlos para cumplir con la normativa de protección de datos (GDPR), y construir un modelo de datos robusto (Star Schema) en Power BI.

🎯 Problema de Negocio
Los Property Managers pierden horas cada semana cruzando Excel de diferentes plataformas.
Dificultad para calcular el RevPAR (Revenue Per Available Room) y el ADR (Average Daily Rate) neto real descontando las comisiones ocultas de cada OTA (Online Travel Agency).
Incapacidad para predecir picos de demanda basándose en el "Lead Time" (antelación de reserva históricos).
💡 La Solución (Arquitectura)
Extracción (Python): Script que se conecta a la API de Smoobu/Booking o procesa archivos CSV exportados.
Transformación y Anonimización (Pandas/Python):
Limpieza de datos nulos.
Hashing/Enmascaramiento de PII (Nombres, emails, teléfonos de huéspedes).
Estandarización de monedas y zonas horarias.
Modelado de Datos (Power BI - Power Query): Creación de un Tabular Data Model en esquema de estrella separando Tablas de Hechos (Reservas, Transacciones) de Tablas de Dimensiones (Calendario, Propiedades, Canales).
Visualización (Power BI - DAX): Dashboard interactivo con métricas dinámicas (Time Intelligence YoY, MoM).
🛠️ Stack Tecnológico
Lenguajes: Python (Pandas), DAX, M, SQL (Opcional si se usa base de datos intermedia).
BI & Visualización: Microsoft Power BI.
APIs: Integración REST API (Smoobu / Booking).
📈 KPIs Principales a Monitorizar
ADR (Average Daily Rate): Tarifa media diaria bruta vs. neta.
RevPAR: Ingreso por habitación disponible.
Dependency Ratio: % de dependencia de Booking.com frente a reservas directas.
Cancellation Rate: Tasa de cancelación segmentada por canal y Lead Time.
🚀 Próximos Pasos (Roadmap de Ejecución)
 Fase 1: Obtener un dump inicial de datos (CSV) de Smoobu y analizar la estructura.
 Fase 2: Crear el script de Python en Google Colab/Jupyter para la limpieza y anonimización de datos reales.
 Fase 3: Diseñar el modelo relacional teórico.
 Fase 4: Importar datos en Power BI y escribir las fórmulas DAX core.
 Fase 5: Diseño UI/UX del Dashboard y publicación en NovyPro.
