# API Centro de Treinamento

API REST desenvolvida com FastAPI para gerenciamento de atletas, categorias e centros de treinamento.

## Tecnologias utilizadas

* Python 3.11+
* FastAPI
* SQLAlchemy 2.0
* Alembic
* PostgreSQL
* AsyncPG
* Uvicorn
* Pydantic

---

# Estrutura do Projeto

```text
API-CentroDeTreinamento/
├── alembic/
├── workout_api/
│   ├── atleta/
│   ├── categorias/
│   ├── centro_treinamento/
│   ├── configs/
│   ├── contrib/
│   ├── main.py
│   └── routers.py
├── alembic.ini
├── docker-compose.yml
├── Makefile
├── requirements.txt
└── README.md
```

---

# Funcionalidades

* Cadastro de atletas
* Listagem de atletas
* Atualização de atletas
* Remoção de atletas
* Cadastro de categorias
* Cadastro de centros de treinamento
* Integração com PostgreSQL
* Migrations com Alembic
* Documentação automática com Swagger

---

# Configuração do Ambiente

## 1. Clone o repositório

```bash
git clone https://github.com/WABarreto/API-CentroDeTreinamento
cd API-CentroDeTreinamento
```

---

## 2. Crie o ambiente virtual

### Windows

```powershell
py -m venv .venv
```

Ative o ambiente:

```powershell
.venv\Scripts\activate
```

### Linux/macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
```

---

## 3. Instale as dependências

```bash
pip install -r requirements.txt
```

---

# Configuração do Banco de Dados

Instale o PostgreSQL:

[https://www.postgresql.org/download/](https://www.postgresql.org/download/)

Crie um banco de dados:

```sql
CREATE DATABASE workout_api;
```

---

# Configuração da URL do Banco

Configure a URL de conexão no projeto.

Exemplo:

```python
DATABASE_URL = "postgresql+asyncpg://postgres:senha@localhost:5432/workout_api"
```

---

# Executando as Migrations

## Criar migration

```bash
alembic revision --autogenerate -m "init_db"
```

## Aplicar migrations

```bash
alembic upgrade head
```

---

# Executando a Aplicação

```bash
uvicorn workout_api.main:app --reload
```

A aplicação estará disponível em:

```text
http://127.0.0.1:8000
```

---

# Documentação da API

Swagger:

```text
http://127.0.0.1:8000/docs
```

Redoc:

```text
http://127.0.0.1:8000/redoc
```

# Autor

Projeto desenvolvido para fins de estudo e treinamento com FastAPI.
