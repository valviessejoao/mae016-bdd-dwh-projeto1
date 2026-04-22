# 📊 Projeto de Banco de Dados e Data Warehouse

**Locadora de Veículos**

---

## 📚 Disciplina

**Banco de Dados e Data Warehouse - MAE016** \
**Universidade Federal do Rio de Janeiro - UFRJ**

---

## 👥 Integrante

**João Valviesse Peclat Brito - 115065139**

---

## 🎯 Objetivo do Projeto

Este projeto tem como objetivo o desenvolvimento de um **Banco de Dados Relacional (OLTP)** para uma locadora de veículos, bem como a sua preparação para integração futura em um **Data Warehouse (DW)** corporativo.

O cenário proposto envolve um grupo de seis empresas independentes que decidiram compartilhar seus pátios, mantendo seus sistemas transacionais próprios, mas possibilitando a análise integrada dos dados históricos.

---

## 🧩 Escopo do Sistema

O banco de dados modelado contempla os principais processos do negócio de locação de veículos:

* Cadastro de clientes (Pessoa Física e Jurídica)
* Cadastro de condutores
* Gestão da frota de veículos
* Classificação por grupos/categorias de veículos
* Controle de pátios
* Reservas de veículos
* Locações
* Controle de retirada e devolução
* Cobrança e pagamentos
* Movimentação de veículos entre pátios

---

## 🏗️ Estrutura do Repositório

```text
mae016-bdd-dwh-projeto1/
│
├── README.md
│
├── docs/
│   ├── 01_descricao_projeto.pdf
│   ├── 02_dicionario_de_dados.pdf
│   ├── 03_modelo_conceitual.png
│   ├── 04_modelo_logico.png
│
├── sql/
│   ├── 01_create_tables.sql
│   ├── 02_constraints.sql

```

---

## 📄 Documentação

### 🔹 1. Texto do Projeto (`docs/01_texto_projeto.pdf`)

Descrição completa do sistema, incluindo:

* Contexto do problema
* Escopo do banco de dados
* Regras de negócio

---

### 🔹 2. Dicionário de Dados (`docs/02_dicionario_de_dados.pdf`)

Detalhamento de todas as tabelas e atributos:

* Tipos de dados
* Chaves primárias e estrangeiras
* Descrição funcional de cada campo

---

### 🔹 3. Modelo Conceitual (`docs/03_modelo_conceitual.png`)

Diagrama Entidade-Relacionamento (MER), contendo:

* Entidades
* Relacionamentos
* Cardinalidades

---

### 🔹 4. Modelo Lógico (`docs/04_modelo_logico.png`)

Representação relacional do modelo, incluindo:

* Tabelas
* Chaves primárias
* Chaves estrangeiras

---

## 🗄️ Scripts SQL

### 🔹 `01_create_tables.sql`

Criação das tabelas do banco de dados.

### 🔹 `02_constraints.sql`

Definição de:

* Chaves estrangeiras
* Regras de integridade

---

## 🔄 Integração com Data Warehouse

O modelo transacional foi estruturado de forma a facilitar processos de ETL e posterior integração em um Data Warehouse corporativo.

Os principais pontos de integração são:

* **Reservas → Fato de Reservas**
* **Locações → Fato de Locações**
* **Clientes, Veículos, Grupos e Pátios → Dimensões**

Essa estrutura permite a construção de relatórios gerenciais globais e análises unificadas entre as empresas do grupo.

---

## 📌 Observações

* O modelo foi construído considerando um único sistema transacional, representando uma das empresas do grupo.
* A integração entre empresas ocorre no nível analítico (Data Warehouse).
* O foco do projeto está na consistência dos dados e na capacidade de suportar análises gerenciais.

---