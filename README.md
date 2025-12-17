# TaskFlow API

[![Status](https://img.shields.io/badge/status-development-yellow)]()
[![License](https://img.shields.io/badge/license-MIT-blue)]()

**Uma plataforma de gerenciamento de tarefas e fluxos de trabalho colaborativos com integração de inteligência artificial para análise de produtividade.**

## 🎯 Objetivo

Demonstrar capacidades em:
- ✅ APIs REST seguindo os bons princípios do mercado
- ✅ OpenAPI 3.0 + Swagger para documentação
- ✅ Segurança com JWT, OAuth2, Rate Limiting e CORS
- ✅ Performance com Redis, tunning JVM e profiling
- ✅ Integração assíncrona com RabbitMQ
- ✅ Versionamento de API (v1/v2)

## 🏗️ Stack Técnico

| Componente | Tecnologia |
|-----------|-----------|
| Framework | Spring Boot 3.4 |
| Java | 21 LTS |
| Banco de Dados | PostgreSQL 15 |
| Cache | Redis 7 |
| Message Queue | RabbitMQ 3.12 |
| API Documentation | OpenAPI 3.0 + Springdoc |
| Autenticação | JWT + OAuth2 |
| Rate Limiting | Bucket4j |
| Testes | JUnit 5 + Testcontainers |
| Build | Maven 3.9 |

## 🚀 Quick Start

### Pré-requisitos
- Java 21+
- Docker e Docker Compose
- Maven 3.9+

### Setup Local

```bash
# Clone o repositório
git clone https://github.com/M41k0n-Mk/taskflow-api.git
cd taskflow-api

# Inicie dependências (PostgreSQL, Redis, RabbitMQ)
docker-compose up -d

# Build do projeto
mvn clean install

# Execute a aplicação
mvn spring-boot:run
```

### Acessar Swagger
- http://localhost:8080/swagger-ui.html

## 📋 Funcionalidades Principais

### Core
- ✅ CRUD de projetos, tarefas e subtarefas
- ✅ Colaboração de usuários com comentários
- ✅ Histórico de atividades (audit log)
- ✅ Soft deletes para auditoria

### API Versionamento
- ✅ v1: Estrutura legada mantida para compatibilidade
- ✅ v2: Estrutura moderna com melhorias

### Segurança
- ✅ JWT com refresh tokens
- ✅ OAuth2 (Google login)
- ✅ Rate limiting por usuário/IP
- ✅ CORS configurável por ambiente

### Performance
- ✅ Cache em Redis (5min TTL)
- ✅ Lazy loading no Hibernate
- ✅ Query optimization (n+1 prevention)
- ✅ JVM tuning profiles

### Integração Assíncrona
- ✅ RabbitMQ queues para notificações
- ✅ Relatórios em background
- ✅ Analytics em tempo real
- ✅ Dead letter queues

## 📁 Estrutura do Projeto

```
taskflow-api/
├── src/main/java/com/taskflow/
│   ├── api/
│   │   ├── v1/                    # Endpoints v1
│   │   └── v2/                    # Endpoints v2
│   ├── auth/                      # JWT, OAuth2
│   ├── domain/                    # Entities
│   ├── service/                   # Lógica de negócio
│   ├── repository/                # Data access
│   ├── config/                    # Redis, RabbitMQ, Security
│   ├── queue/                     # Consumers
│   ├── aspect/                    # AOP (Rate Limiting, Cache)
│   └── exception/                 # Global exception handler
├── docs/
│   ├── openapi.yaml
│   ├── ARCHITECTURE.md
│   ├── PERFORMANCE.md
│   └── SECURITY.md
├── scripts/
│   ├── docker-compose.yml
│   └── init-db.sql
├── jvm-profiles/
│   └── jvm.options
└── pom.xml
```

## 🔗 Relação com Outros Repos

- **[taskflow-intelligence-lambda](https://github.com/M41k0n-Mk/taskflow-intelligence-lambda)**: Serviço Python que consome eventos da API via RabbitMQ para análise de inteligência artificial
- **[taskflow-client](https://github.com/M41k0n-Mk/taskflow-client)**: Cliente TypeScript/React que consome a API

## 📊 Roadmap

- **Semana 1-2**: Setup Spring Boot, PostgreSQL, estrutura base
- **Semana 3**: JWT, OAuth2, Rate Limiting, CORS
- **Semana 4**: Redis, cache strategies, JVM tuning
- **Semana 5-6**: RabbitMQ, integração, Lambda
- **Semana 7**: Documentação, profiling, polish

## 🤝 Como Contribuir

Este projeto é um portfolio técnico. Sinta-se livre para fork e adaptar!

## 📝 Licença

MIT License - veja LICENSE para detalhes

---

**Criado com ❤️ para demonstrar melhores práticas em arquitetura de APIs REST**

