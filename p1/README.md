# Pràctica 1: Intal·lació i configuració
Joan Puigcerver Ibáñez

## Instal·lació de PostgreSQL
Hem utilitzat Docker per crear un contenidor de PostgreSQL i ...

```yaml
services:
  oracle-db:
    container_name: oracleX213
    image: container-registry.oracle.com/database/express:21.3.0-xe
    environment:
      - ORACLE_PWD=oracle
    ports:
      - 1521:1521
      - 5500:5500
      - 8080:8080
    # volumes:
    #   - ./oradata:/opt/oracle/oradata
    ulimits:
      nofile:
        soft: 65536
        hard: 65536
```