# Liquibase Lab

Este proyecto es un entorno de laboratorio para gestionar y versionar bases de datos PostgreSQL utilizando [Liquibase](https://www.liquibase.org/) y [Docker Compose](https://docs.docker.com/compose/).

## ¿Qué es Liquibase?

Liquibase es una herramienta de código abierto para el control de versiones de bases de datos. Permite aplicar cambios estructurados (changelogs) de manera segura y repetible.

## Tecnologías utilizadas

- **Liquibase:** Para gestionar los cambios en la base de datos.
- **PostgreSQL:** Motor de base de datos relacional.
- **Docker Compose:** Orquestador para levantar los servicios de manera sencilla y reproducible.

## ¿Cómo funciona?

1. **Docker Compose** levanta un contenedor de PostgreSQL y otro de Liquibase.
2. Los scripts de cambios de base de datos (changelogs) se aplican automáticamente usando Liquibase.
3. Puedes modificar los changelogs para evolucionar el esquema de la base de datos de forma controlada.

## Uso rápido

```bash
docker exec -it liquibase_cli liquibase update
```

Esto iniciará los servicios y aplicará los cambios definidos en los changelogs de Liquibase sobre la base de datos PostgreSQL.

## Estructura del proyecto

- `docker-compose.yml`: Define los servicios de PostgreSQL y Liquibase.
- `changelogs/`: Carpeta donde se almacenan los archivos de cambios de Liquibase.

## Requisitos

- Docker
- Docker Compose
