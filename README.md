# API REST - Gerenciamento de Alunos

API REST desenvolvida em Go com Gin Framework para gerenciar cadastro de alunos.

## 🚀 Tecnologias

- **Go 1.20+** - Linguagem de programação
- **Gin** - Framework web
- **GORM** - ORM para PostgreSQL
- **PostgreSQL 16** - Banco de dados
- **Docker & Docker Compose** - Containerização
- **GitHub Actions** - CI/CD

## 📋 Pré-requisitos

- Go 1.18 ou superior
- Docker & Docker Compose
- Git

## ⚙️ Configuração

### 1. Clonar o repositório

```bash
git clone https://github.com/apariciodevsf/Curso_CI_2.git
cd Curso_CI_2
```

### 2. Configurar variáveis de ambiente

```bash
cp .env.example .env
```

Edite o arquivo `.env` se necessário (valores padrão já funcionam).

### 3. Subir o banco de dados

```bash
docker-compose up -d
```

### 4. Instalar dependências

```bash
go mod download
```

### 5. Executar a aplicação

```bash
go run main.go
```

A API estará disponível em: `http://localhost:8080`

## 📡 Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| GET | `/:nome` | Saudação personalizada |
| GET | `/alunos` | Lista todos os alunos |
| GET | `/alunos/:id` | Busca aluno por ID |
| GET | `/alunos/cpf/:cpf` | Busca aluno por CPF |
| POST | `/alunos` | Cria novo aluno |
| PATCH | `/alunos/:id` | Atualiza aluno |
| DELETE | `/alunos/:id` | Remove aluno |
| GET | `/index` | Interface HTML |

## 📦 Modelo de Dados

```json
{
  "nome": "string (obrigatório)",
  "rg": "string (9 dígitos)",
  "cpf": "string (11 dígitos)"
}
```

## 🧪 Testes

### Executar testes

```bash
go test -v main_test.go
```

### Postman Collection

Importe o arquivo `API-Alunos-Postman.json` no Postman para testar todos os endpoints.

## 🐳 Docker

### Serviços disponíveis

- **PostgreSQL**: `localhost:5432`
- **PgAdmin**: `http://localhost:54321`
  - Email: `aparicio.junior@example.com`
  - Senha: `admin123`

## 🔄 CI/CD

O projeto utiliza GitHub Actions para:
- ✅ Executar testes automaticamente
- ✅ Build da aplicação
- ✅ Criar e publicar imagem Docker

## 📝 Variáveis de Ambiente

| Variável | Descrição | Padrão |
|----------|-----------|--------|
| HOST | Host do PostgreSQL | localhost |
| DB_PORT | Porta do PostgreSQL | 5432 |
| USER | Usuário do banco | root |
| PASSWORD | Senha do banco | root |
| DBNAME | Nome do banco | root |

## 📄 Licença

Este projeto é open source e está disponível sob a licença MIT.

## 👤 Autor

**Aparicio Junior**
- GitHub: [@apariciodevsf](https://github.com/apariciodevsf)
- Docker Hub: [apariciojunior](https://hub.docker.com/u/apariciojunior)
