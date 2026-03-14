# Laboratório Docker: Ambiente de Desenvolvimento Full-Stack

Ambiente de desenvolvimento completo e containerizado criado com Docker Compose, contendo:
* Frontend React (Vite)
* Backend NestJS
* Banco de dados PostgreSQL
* Gerenciamento de banco com PGAdmin
* Proxy reverso Nginx

## Como iniciar o ambiente

1. Copie o arquivo de exemplo de variáveis de ambiente:
```bash
cp .env.example .env
```

2. Construa e inicie os containers em segundo plano:
```bash
docker-compose up --build -d
```

## Como acessar os serviços

* **Aplicação Completa (via Nginx):** `http://localhost:8080` (Acesso ao Frontend React)
* **API (via Nginx):** `http://localhost:8080/api` (Acesso ao Backend NestJS)
* **Frontend (Acesso Direto):** `http://localhost:5173`
* **Backend (Acesso Direto):** `http://localhost:3000`
* **PGAdmin:** `http://localhost:5550`

### Acesso ao Banco de Dados (PGAdmin)
* **E-mail:** Utilize o `PGADMIN_DEFAULT_EMAIL` definido no arquivo `.env`
* **Senha:** Utilize a `PGADMIN_DEFAULT_PASSWORD` definida no arquivo `.env`
* **Host para conexão interna:** `postgres`
