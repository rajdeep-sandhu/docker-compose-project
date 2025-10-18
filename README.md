# Docker Compose Project

- These are project files for the [Learning Docker Compose](https://www.linkedin.com/learning/learning-docker-compose/implement-docker-compose) course, which is part of the **Docker Foundations Certification**.

## Files

- The project is organised under the `kineteco` directory.
- `docker-compose.yaml`: Docker Compose file.
- `storefront`, `scheduler` and `mysql` files.
- `./mysql/env_vars`: Environment variables for MySQL, including credentials. In a real world scenario, secrets **should not** be committed to version control.

## Port mappings

- Both the `scheduler` and `storefront` service expose port `80` as `80` and `81` respectively.
- The `storefront` service reports monitoring information on port `443`. A collection agent runs on the host machine on the same port.

## Sevice dependencies

- The `database` service should be running before the `storefront` service.
