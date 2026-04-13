# Motor de Notificaciones en Tiempo Real - Red Social

## 1. Descripción del Proyecto
Este sistema está diseñado para procesar interacciones de usuarios (likes, comentarios, seguidores) y enviar notificaciones instantáneas.  
Dado que el equipo de producto requiere iteraciones constantes cada dos semanas, el sistema se ha construido para ser modular, escalable y fácil de actualizar basándose en métricas de uso y feedback directo.

## 2. Arquitectura Seleccionada
Se ha implementado una **Arquitectura Lambda**:

* **Capa de Velocidad (Speed Layer):** Procesa eventos en tiempo real para envíos inmediatos de notificaciones.
* **Capa de Lote (Batch Layer):** Almacena el historial de interacciones para generar reportes analíticos y métricas de comportamiento cada ciclo de 2 semanas.

## 3. Requisitos y Configuración del Entorno Técnico
Para ejecutar este proyecto, es necesario contar con las siguientes herramientas instaladas:

* **Git:** Para el control de versiones del código.
* **Docker & Docker Compose:** Para orquestar los servicios de Kafka, Redis y bases de datos.
* **Python 3.10+:** Lenguaje principal para la lógica de procesamiento.
* **Apache Kafka:** Plataforma de streaming para la ingesta de interacciones.
* **Redis:** Memoria volátil para el almacenamiento rápido de estados de notificación.

## 4. Instrucciones de Instalación
Siga estos pasos para configurar el entorno local:

1. **Clonar el repositorio:**
   ```bash
   https://github.com/tedementall/motor-notificaciones-red-social
   
