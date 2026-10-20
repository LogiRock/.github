# 🚀 LogiRock | Shipment Microservice

![Java](https://img.shields.io/badge/Java-25-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![JUnit5](https://img.shields.io/badge/JUnit5-%26_Mockito-25A162?style=for-the-badge&logo=junit5&logoColor=white)

Microservicio de logística backend diseñado para la gestión integral de envíos, administración de repartidores y control de clientes. Construido bajo una arquitectura limpia, contenerizada y orientada a la escalabilidad.

---

## 📌 Características Principales (Sprint 1)

*   📦 **Gestión de Envíos:** Administración del ciclo de vida de los paquetes, modelando rutas mediante el uso de *Value Objects* (`Direccion`) embebidos para origen y destino.
*   🛵 **Administración de Repartidores:** Control de flota y estados operativos mediante enumeraciones estrictas.
*   👥 **Módulo de Clientes:** Registro y auditoría automática de usuarios del sistema logístico.
*   🛡️ **Manejo Global de Excepciones:** Interceptor centralizado (`@RestControllerAdvice`) que estandariza las respuestas de error (400, 404, 409, 500) y protege las trazas internas mediante auditoría con SLF4J.
*   🧪 **Testing Aislado:** Pruebas unitarias puras implementadas con Mockito, aislando la capa web y de persistencia para garantizar ejecuciones rápidas y confiables.

## ⚙️ Arquitectura y Estándares

El proyecto fue desarrollado siguiendo estrictos estándares de calidad técnica acordados por el equipo:

*   **Código Limpio:** Ausencia total de comentarios en línea (*inline comments*). Todo el código base, entidades, interfaces y controladores están documentados exclusivamente mediante **Javadocs** bajo estándares profesionales.
*   **Persistencia:** Uso de Spring Data JPA con Hibernate. Implementación de IDs basados en `UUID` y herencia de auditoría (`@MappedSuperclass`) para control automático de fechas de creación y modificación.
*   **Flujo de Trabajo:** Estrategia de ramificación basada en Git, donde todo el desarrollo se integra progresivamente en la rama `developer` antes de pasar a producción.

---

## 🐳 Despliegue Local (Docker)

El entorno de base de datos y la aplicación están completamente contenerizados para evitar problemas de compatibilidad (funcional sobre WSL2/Windows y Linux).

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/logirock.git](https://github.com/tu-usuario/logirock.git)
   cd logirock
   ```

2. **Levantar los servicios:**
   Asegurate de no tener instancias previas corruptas y ejecutá:
   ```bash
   docker-compose down -v
   docker-compose up -d --build
   ```

3. **Verificar ejecución:**
   El microservicio estará disponible en `http://localhost:8080`.

---

## 👥 Equipo de Desarrollo

| Habilidad / Conocimiento | Maximiliano Flores | Jose Fernandez | Florencia Fuentes |
| :--- | :--- | :--- | :--- |
| **Desarrollo Backend** <br>(Java 25 / Spring Boot 3.x) | **Avanzado** <br>(6 años de experiencia). | **Avanzado** <br>(6 años de experiencia). | **Inicial** <br>(En proceso de aprendizaje y adaptación). |
| **Persistencia y Dominio Relacional** <br>(JPA / Hibernate / MySQL) | **Avanzado** <br>(Modelado de entidades, UUID y auditoría). | **Avanzado** <br>(Modelado de entidades, UUID y auditoría). | **Inicial** <br>(En proceso de aprendizaje y adaptación). |
| **Diseño de APIs REST** <br>(DTOs / @RestControllerAdvice) | **Avanzado** <br>(Desacoplamiento y manejo global de errores). | **Avanzado** <br>(Desacoplamiento y manejo global de errores). | **Inicial** <br>(En proceso de aprendizaje y adaptación). |
| **Infraestructura y Contenedores** <br>(Dockerfile / Docker Compose) | **Avanzado** <br>(Construcción multi-stage y entornos aislados). | **Avanzado** <br>(Construcción multi-stage y entornos aislados). | **Inicial** <br>(En proceso de aprendizaje y adaptación). |
| **Control de Versiones y Gestión** <br>(Git / GitHub Projects) | **Avanzado** <br>(Uso de ramas y flujos Kanban). | **Avanzado** <br>(Uso de ramas y flujos Kanban). | **Intermedio** <br>(Manejo adecuado de repositorios y commits). |
| **Testing Automatizado** <br>(JUnit 5 / Mockito / Integración) | **Inicial** <br>(Con disposición para aprender y aplicar en la máquina de estados). | **Inicial** <br>(Con disposición para aprender y aplicar en la máquina de estados). | **Inicial** <br>(En proceso de aprendizaje y adaptación). |
| **Presentación y Comunicación** <br>(Video Explicativo) | **Avanzado** <br>(Disponible para la locución y presentación de la entrega de la cátedra). | **Avanzado** <br>(Disponible para la locución y presentación de la entrega de la cátedra). | **Intermedio** <br>(Apoyo en la estructuración y armado de la presentación). |
