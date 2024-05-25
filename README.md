# Ejecutar en prod

1. Copiar el archivo .env.example y renombrar a .env - rellenar los datos

2. Crear network de docker
```
docker network odoo-network
```

3. Run
```
docker-compose up -d
```

4. Crear db inicial de odoo
```
docker-compose down odoo
docker-compose run --rm odoo odoo -i base
ctrl + c
docker-compose restart
```