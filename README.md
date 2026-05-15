# Event & Ticketing Microservices Platform

Una solución integral para la creación de eventos y venta de entradas, construida bajo una arquitectura de microservicios escalable y orientada a procesos de negocio.

## Arquitectura y Componentes
El sistema utiliza un enfoque de microservicios para garantizar la independencia y escalabilidad:

* **API Gateway:** Punto de entrada único con Spring Cloud Gateway.
* **Orquestación BPM:** Uso de **Camunda 7** para modelar y ejecutar procesos complejos (Sagas).
* **Servicios Core:** Gestión de Usuarios (Auth JWT), Eventos, Tickets, Pagos y Notificaciones.
* **Frontend:** Aplicación moderna en React + Tailwind CSS.

## Características Principales
* **Flujos Orquestados:** Procesos de compra y registro automatizados mediante BPMN.
* **Seguridad:** Autenticación basada en roles y protección de rutas mediante JWT.
* **Gestión de Imágenes:** Servicio dedicado para la carga y almacenamiento de portadas de eventos.
* **Resiliencia:** Implementación de reintentos y manejo de errores estandarizado en la red de servicios.

## Stack Tecnológico
* **Backend:** Java 17, Spring Boot 3, Spring Data JPA.
* **BPM:** Camunda Platform 7.
* **Frontend:** React, Vite, Tailwind CSS.
* **Base de Datos:** PostgreSQL / MySQL (vía Docker).
* **DevOps:** Docker, Docker Compose.

## Despliegue Rápido
Para levantar todo el ecosistema de microservicios:

1. Clonar el repositorio.
2. Ejecutar el script de inicio (requiere Docker):
   ```bash
   ./Services/start-services.ps1
3. Acceder al Frontend en http://localhost:5173 y al Gateway en http://localhost:8080.

Nota
Este proyecto fue desarrollado como parte de mi formación en Ingeniería de Sistemas e Informática, demostrando habilidades en el diseño de sistemas distribuidos, comunicación asíncrona entre servicios y automatización de procesos empresariales (BPM).
