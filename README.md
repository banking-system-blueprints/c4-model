# Banking System Blueprints

**Architecture of Integration in Banking & Fintech Software**

Este repositorio contiene la arquitectura de referencia para una plataforma bancaria moderna, diseñada como un proyecto de Investigación y Desarrollo (R&D) utilizando [LikeC4](https://likec4.dev/).

El objetivo es proporcionar un conjunto de "planos" arquitectónicos (blueprints) que modelen la complejidad técnica de la transformación digital bancaria, sirviendo como recurso para arquitectos de software, ingenieros de integración y equipos técnicos en el sector financiero.

> [!IMPORTANT]
> **Diseño de Solución Completo**: El documento detallado con el diseño de solución aplicado se encuentra disponible en PDF:
> 📄 [**Diseño de Solución.pdf**](docs/Diseño%20de%20Solución.pdf)

## 🏛️ Visión Técnica

Este modelo propone una arquitectura de referencia agnóstica de proveedor, centrada en la interoperabilidad y la escalabilidad financiera:

- **Arquitectura Orientada a Eventos (EDA)**: Desacoplamiento de sistemas transaccionales mediante buses de eventos distribuidos para garantizar consistencia eventual e integridad de datos.
- **Seguridad de Grado Financiero**: Adopción de estándares abiertos (OAuth2, OIDC, FAPI) para el intercambio seguro de datos y la gestión federada de identidades.
- **Estrategia de Coexistencia Híbrida**: Patrones de integración (Strangler Fig, CDC) que permiten la evolución de plataformas digitales modernas manteniendo la operatividad de sistemas de registro heredados.
- **Inteligencia en Tiempo Real**: Ingesta y procesamiento de datos de alta velocidad para la toma de decisiones críticas (riesgo, fraude, personalización) con latencias mínimas.

## 🚀 Despliegue y Ejecución

El proyecto está contenerizado para facilitar su despliegue en cualquier entorno compatible con OCI (Docker, K8s).

### Opción A: Ejecución con Docker (Recomendado)

Construya y ejecute la imagen del contenedor para visualizar los diagramas:

```bash
# 1. Construir la imagen
docker build -t banking-blueprints .

# 2. Ejecutar el contenedor
docker run -p 8080:80 banking-blueprints
```

Acceda a la arquitectura en: **http://localhost:8080**

### Opción B: Ejecución Local (Desarrollo)

Requisitos: Node.js 18+

```bash
git clone https://github.com/Banking-System-Blueprints/reference-architecture.git
cd banking-system-blueprints
npm install
npm start
```

## 📂 Estructura del Repositorio

```
src/
├── 00_specs.c4    # Especificaciones del lenguaje de diseño (Estilos, Tipos)
├── model.c4       # Modelo de Dominio (Sistemas, Contenedores, Relaciones)
└── views.c4       # Vistas Arquitectónicas (General, Contexto, Flujos)
```

## 🛠️ Stack Tecnológico de Referencia

El modelo asume el uso de tecnologías líderes en la industria:

- **Middleware**: Kong Gateway, Apache Kafka.
- **Seguridad**: Keycloak (OAuth2/OIDC).
- **Backend**: Java 21 (Spring Boot), Python (ML Services).
- **Datos**: PostgreSQL (Transactional), MongoDB (Document), Redis (Cache).

## 📄 Licencia

Este proyecto se distribuye bajo la licencia **MIT**, permitiendo su uso libre tanto en proyectos de investigación como comerciales. Ver archivo [LICENSE](LICENSE) para más detalles.

---

_Banking System Blueprints - Open Architecture Initiative._
