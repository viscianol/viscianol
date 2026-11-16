# Olá, sou o Lucas Visciano Rodrigues 👋

### **Senior Analytics Engineer | Financial Data Platform Engineer**
📍 São Paulo, SP / Brasil (Disponível para oportunidades Remotas ou Híbridas)  
💼 Conectando regras de negócio financeiras complexas a arquiteturas de dados escaláveis, resilientes e de alta performance.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/lucasvisciano)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lucas.visciano@gmail.com)
[![Portfolio Status](https://img.shields.io/badge/Status-Dispon%C3%ADvel%20para%20Novos%20Desafios-success?style=for-the-badge)]()

---

## 🎯 Sobre Mim & Visão de Engenharia

Engenheiro de Dados e Analytics Engineer com mais de 7 anos de experiência no ecossistema analítico e financeiro. Com histórico comprovado de alta cadência de entregas em produção em esteiras de CI/CD, atuo na sustentação e evolução contínua de plataformas de dados — cobrindo desde a arquitetura de dados (PostgreSQL, arquitetura Medallion, modelagem dimensional) até a extensão de microsserviços e APIs transacionais.

- 🏗️ **Arquitetura de Plataforma de Dados:** Construção de ecossistemas completos em arquitetura Medallion (*Bronze JSONB imutável com deduplicação por hash SHA-256 e índice GIN; Silver normalizada e idempotente; Gold dimensional com fatos/dimensões multi-entidade e snapshots auditáveis append-only*).
- 💰 **Engenharia Financeira & Finanças Estruturadas:** Domínio em regras de crédito (FIDCs, Risco Sacado, BaaS, conciliação de core bancário e compliance CVM). Desenvolvimento de solvers numéricos de alta complexidade diretamente na camada de dados (Taxa Interna de Retorno - TIR via método de Newton-Halley e modelagem de floating).
- ⚙️ **Software Engineering for Data:** Desenvolvimento de microsserviços e pipelines resilientes com Python (FastAPI), TypeScript (NestJS/Prisma com queries SQL brutas otimizadas e CTEs paralelas), conteinerização com Docker e CI/CD automatizado via GitHub Actions.
- 🤝 **Interlocução C-Level:** Histórico de fechamentos financeiros e auditoria bancária executiva centavo a centavo diretamente com a diretoria.

---

## 🛠️ Tecnologias & Ecossistema

### **Engenharia & Modelagem de Dados**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL](https://img.shields.io/badge/SQL%20Avançado-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white)

- **Padrões de Dados:** Arquitetura Medallion (Bronze/Silver/Gold), Modelagem Dimensional (Star Schema, Snowflake), Upserts Idempotentes por Chave Natural, CDC, Hashing Criptográfico (SHA-256), Backfills Automatizados via CLI (`argparse`).

### **Engenharia de Software & Backend**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white)

- **Boilerplates & Padrões:** Arquitetura Modular (Repository Pattern, Use Cases, DTOs, Factories), Contratos de API (OpenAPI), Autenticação Stateless (HMAC), Integração com APIs Bancárias assinadas criptograficamente.

### **DataOps, Cloud & Visualização**
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

- **Infra & Monitoramento:** Docker Compose, Azure App Service, Azure Key Vault, Linux Cron, APScheduler, Relatórios Automatizados em PDF (ReportLab) e Excel (OpenPyXL).

---

## 🚀 Arquiteturas & Destaques de Produção
```mermaid
flowchart TD
    subgraph S1 ["📥 FONTES & INGESTÃO HETEROGÊNEA"]
        F1["APIs Bancárias (DTVM / BaaS com Chave Criptográfica)"]
        F2["Core Bancário BMP (Web Scraping com TOTP)"]
        F3["Integrações SFTP (URs de Cartão & Serasa)"]
    end

    subgraph S2 ["🏛️ ARQUITETURA MEDALLION (PostgreSQL)"]
        direction TB
        B["🥉 BRONZE: JSONB Imutável, Deduplicação SHA-256 & Índices GIN"]
        S["🥈 SILVER: Normalização Tipada, Idempotência & Backfills CLI"]
        G["🥇 GOLD: Modelagem Dimensão/Fato Multi-Entidade & Snapshots"]
        B --> S --> G
    end

    subgraph S3 ["📊 CAMADA DE CONSUMO & DECISÃO"]
        C1["Dashboards C-Level (Streamlit Multi-Tenant)"]
        C2["Microsserviços & Painéis TV (FastAPI & React/Vite)"]
        C3["Fechamento Financeiro & Conciliação Automatizada (PDF/E-mail)"]
    end

    S1 -->|"Pipelines de Ingestão"| B
    G -->|"Solvers TIR, Métricas CVM & Floating"| S3
```


### Principais Frentes Técnicas Desenvolvidas:
1. **Plataforma de Dados Medallion & Fechamento Financeiro:** Ingestão de APIs de custódia e core bancário com deduplicação por hash, conciliação diária de receitas (tarifas e floating) e geração automática de relatórios executivos para diretoria.
2. **Framework de Dados Modular:** Template de microsserviço corporativo em FastAPI, SQLAlchemy e Alembic, preparado para testes in-memory com SQLite e orquestração de crons via APScheduler.
3. **APIs Transacionais & Geração CNAB 444:** Desenvolvimento de endpoints externos de alta performance em NestJS/Prisma com queries SQL raw em paralelo e motor de geração de arquivos posicionais bancários CNAB 444.
4. **Motor de Simulação & Regras de Negócio (Solo RPG Engine):** Projeto autoral explorando Orientação a Objetos avançada, Design Patterns (State, Factory), controle determinístico de eventos e suíte completa de testes unitários.

---

## 📈 Formação Acadêmica & Certificações

- **Bacharelado em Ciência de Dados** – UNIVESP *(Cursando)*
- **MBA em Gestão Estratégica de Pessoas** – UNOPAR
- **Engenharia de Dados & Cloud Data Lakes** – Alura (Processamento Distribuído, Docker, Bancos Relacionais)
- **Data Science com Python & Análise Quantitativa** – Santander / DIO
- **Inglês:** Avançado (Leitura técnica fluente, comunicação corporativa)

---

## 📫 Vamos Conversar?

Estou ativamente aberto a conexões e novas oportunidades em **Analytics Engineering**, **Engenharia de Dados** e **Arquitetura de Dados em Fintechs**:

- **LinkedIn:** [linkedin.com/in/lucasvisciano](https://linkedin.com/in/lucasvisciano)
- **E-mail:** [lucas.visciano@gmail.com](mailto:lucas.visciano@gmail.com)
- **Localização:** São Paulo, SP (Disponível para atuar Remoto ou Híbrido)
