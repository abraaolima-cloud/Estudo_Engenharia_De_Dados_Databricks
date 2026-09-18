# 📊 Estudos de Engenharia de Dados com Databricks

Repositório criado para documentar meus estudos práticos em **Engenharia de Dados utilizando Databricks**, desenvolvidos durante a **Imersão em Engenharia de Dados da Alura**.

O objetivo deste repositório é registrar minha evolução prática com conceitos e ferramentas utilizados em pipelines modernos de dados, incluindo ingestão, transformação, tratamento, análise, armazenamento e processamento de dados.

> **Nota:** Os notebooks deste repositório foram desenvolvidos como parte dos estudos e atividades da Imersão em Engenharia de Dados da Alura, com adaptações e experimentações realizadas durante o processo de aprendizagem.

---

## 🎯 Objetivos dos estudos

Durante a imersão, os estudos estão direcionados para:

* Compreender o funcionamento de plataformas modernas de dados;
* Utilizar o **Databricks** para processamento e análise de dados;
* Trabalhar com notebooks e ambientes de desenvolvimento para dados;
* Desenvolver pipelines de dados;
* Realizar ingestão e transformação de dados;
* Aplicar técnicas de limpeza e preparação de dados;
* Utilizar **Python** e **SQL** para manipulação de dados;
* Trabalhar com grandes volumes de informações;
* Compreender conceitos de armazenamento e processamento distribuído;
* Explorar conceitos relacionados ao **Apache Spark**;
* Desenvolver consultas analíticas;
* Estruturar dados para consumo e análise;
* Praticar conceitos de Engenharia de Dados na nuvem.

---

## 🏗️ Conceitos e processos estudados

### 1. Ingestão de dados

A primeira etapa consiste na obtenção dos dados a partir de diferentes fontes.

O processo de ingestão envolve:

```text
Fonte de dados
     ↓
Extração
     ↓
Ingestão
     ↓
Armazenamento
```

Durante os estudos são explorados diferentes formatos e formas de disponibilização dos dados para posterior processamento.

Exemplos de fontes e formatos trabalhados:

* Arquivos CSV;
* Arquivos JSON;
* Dados estruturados;
* Dados semiestruturados;
* Bases de dados;
* Dados disponibilizados em ambientes de nuvem.

---

### 2. Armazenamento

Após a ingestão, os dados precisam ser armazenados de forma adequada para processamento e análise.

São estudados conceitos relacionados a:

* Data Lake;
* armazenamento distribuído;
* arquivos Parquet;
* tabelas;
* particionamento;
* organização dos dados;
* persistência dos dados processados.

O armazenamento permite separar a etapa de ingestão das etapas posteriores de transformação e análise.

---

### 3. Processamento de dados

Os dados ingeridos passam por processos de transformação utilizando principalmente **Python, SQL e Apache Spark**.

Entre as operações estudadas estão:

* Seleção de colunas;
* filtros;
* joins;
* agregações;
* agrupamentos;
* ordenação;
* criação de novas colunas;
* tratamento de tipos;
* transformação de dados;
* remoção de registros inconsistentes;
* tratamento de valores ausentes;
* padronização das informações.

Fluxo simplificado:

```text
Dados brutos
     ↓
Leitura
     ↓
Transformação
     ↓
Validação
     ↓
Dados tratados
```

---

## 🥉🥈🥇 Arquitetura Medallion

Um dos conceitos estudados é a organização dos dados utilizando a **Medallion Architecture**, dividindo o processamento em diferentes camadas.

### 🥉 Bronze

Camada responsável pela entrada dos dados.

Características:

* Dados próximos ao formato original;
* preservação das informações de origem;
* ingestão inicial;
* menor nível de transformação.

```text
Fonte → Bronze
```

### 🥈 Silver

Camada responsável pelo tratamento e organização dos dados.

Processos:

* limpeza;
* padronização;
* tratamento de valores nulos;
* correção de tipos;
* remoção de inconsistências;
* aplicação de regras de negócio;
* integração entre diferentes fontes.

```text
Bronze → Tratamento → Silver
```

### 🥇 Gold

Camada destinada aos dados preparados para consumo analítico.

Processos:

* agregações;
* métricas;
* indicadores;
* tabelas analíticas;
* dados preparados para BI;
* consultas de negócio.

```text
Silver → Agregações → Gold → Analytics / BI
```

Fluxo completo:

```text
             ┌─────────────┐
             │ Fontes      │
             └──────┬──────┘
                    ↓
             ┌─────────────┐
             │   Bronze    │
             │ Dados brutos│
             └──────┬──────┘
                    ↓
             ┌─────────────┐
             │   Silver    │
             │ Dados tratados│
             └──────┬──────┘
                    ↓
             ┌─────────────┐
             │    Gold     │
             │ Dados analíticos│
             └──────┬──────┘
                    ↓
             ┌─────────────┐
             │ Analytics / │
             │     BI      │
             └─────────────┘
```

---

## ⚡ Databricks

O **Databricks** é utilizado como ambiente central dos estudos, permitindo trabalhar com notebooks, processamento de dados e tecnologias do ecossistema Apache Spark.

Os notebooks são utilizados para:

* desenvolvimento;
* execução de código;
* exploração de dados;
* transformação;
* consultas SQL;
* documentação;
* testes;
* análise dos resultados.

---

## 🐍 Python

Python é utilizado para manipulação e processamento dos dados.

Principais conceitos praticados:

* variáveis;
* estruturas de dados;
* funções;
* estruturas de repetição;
* tratamento de dados;
* leitura de arquivos;
* manipulação de DataFrames;
* operações com dados;
* integração com bibliotecas de dados.

Também são explorados recursos relacionados ao processamento distribuído utilizando Spark.

---

## 🔥 Apache Spark

Os estudos também abordam conceitos fundamentais do **Apache Spark**, incluindo processamento distribuído e manipulação de grandes volumes de dados.

Entre os conceitos praticados:

* DataFrames;
* Spark SQL;
* transformações;
* ações;
* filtros;
* joins;
* agregações;
* particionamento;
* processamento distribuído.

A ideia é compreender como operações sobre dados podem ser executadas de forma distribuída em um ambiente de processamento.

---

## 🗃️ SQL

SQL é utilizado para consultas e transformação dos dados.

Entre as operações estudadas:

```sql
SELECT
FROM
WHERE
GROUP BY
ORDER BY
JOIN
```

Também são praticadas:

* agregações;
* filtros;
* criação de consultas analíticas;
* relacionamento entre tabelas;
* transformação de dados;
* análise exploratória.

---

## 🔍 Qualidade e tratamento dos dados

Uma parte importante do processo de Engenharia de Dados é garantir que os dados estejam adequados para utilização.

Os estudos abordam:

* identificação de valores nulos;
* duplicidades;
* inconsistências;
* tipos de dados;
* padronização;
* validação;
* integridade;
* tratamento de dados ausentes;
* conferência dos resultados após transformações.

Fluxo:

```text
Dados recebidos
      ↓
Validação
      ↓
Identificação de problemas
      ↓
Tratamento
      ↓
Nova validação
      ↓
Dados confiáveis
```

---

## 📈 Análise dos dados

Após o tratamento, os dados podem ser utilizados para análises exploratórias e geração de informações.

São praticados:

* exploração de DataFrames;
* estatísticas descritivas;
* agrupamentos;
* análise de distribuição;
* identificação de padrões;
* criação de métricas;
* consultas analíticas.

O objetivo é transformar dados processados em informações que possam apoiar análises e decisões.

---

## 🔄 Pipeline de dados

De forma geral, os estudos permitem compreender o ciclo de um pipeline de dados:

```text
┌──────────────┐
│ Fontes       │
│ de dados     │
└──────┬───────┘
       ↓
┌──────────────┐
│ Ingestão     │
└──────┬───────┘
       ↓
┌──────────────┐
│ Bronze       │
└──────┬───────┘
       ↓
┌──────────────┐
│ Transformação│
└──────┬───────┘
       ↓
┌──────────────┐
│ Silver       │
└──────┬───────┘
       ↓
┌──────────────┐
│ Agregação    │
└──────┬───────┘
       ↓
┌──────────────┐
│ Gold         │
└──────┬───────┘
       ↓
┌──────────────┐
│ Analytics /  │
│ BI           │
└──────────────┘
```

---

## 📂 Estrutura do repositório

```text
.
├── notebooks/
│   ├── notebook-01
│   ├── notebook-02
│   ├── notebook-03
│   └── ...
│
├── README.md
└── ...
```

Os notebooks estão organizados de acordo com a sequência dos estudos realizados durante a imersão.

Cada notebook apresenta uma etapa prática do aprendizado, permitindo acompanhar a evolução dos conceitos de Engenharia de Dados.

---

## 🧰 Tecnologias utilizadas

| Tecnologia   | Utilização                                  |
| ------------ | ------------------------------------------- |
| Databricks   | Ambiente de desenvolvimento e processamento |
| Apache Spark | Processamento distribuído                   |
| PySpark      | Manipulação de dados com Spark              |
| Python       | Programação e tratamento de dados           |
| SQL          | Consultas e transformação                   |
| DataFrames   | Estrutura para manipulação dos dados        |
| Parquet      | Armazenamento de dados                      |
| Git/GitHub   | Versionamento e documentação                |

---

## 📚 Aprendizados

A principal finalidade deste repositório é consolidar conhecimentos práticos em Engenharia de Dados e documentar minha evolução técnica.

Os estudos permitem conectar conceitos de:

**Dados → Engenharia de Dados → Cloud → Processamento Distribuído → Analytics**

Além do conteúdo da imersão, o repositório poderá receber novos notebooks, experimentos e projetos desenvolvidos durante minha evolução nos estudos de **Python, SQL, Databricks, Spark, Cloud, Data Engineering e Inteligência Artificial**.

---

## 🚀 Próximos passos

Como continuidade dos estudos, pretendo aprofundar:

* Apache Spark;
* PySpark;
* Delta Lake;
* Databricks;
* Engenharia de Dados em Cloud;
* Azure;
* ETL/ELT;
* Data Lake;
* Data Warehouse;
* Orquestração de pipelines;
* Qualidade de dados;
* Monitoramento de pipelines;
* CI/CD para dados;
* Modelagem de dados;
* Engenharia de Dados aplicada a projetos reais.

---

## 🎓 Formação e estudos

Este repositório faz parte da minha jornada de desenvolvimento profissional em **Dados e Engenharia de Dados**, complementando minha experiência profissional em tecnologia, SQL, integração de sistemas, implantação de soluções, automação e análise de dados.

**Estudo principal:**
Imersão em Engenharia de Dados — Alura

**Áreas de interesse:**
Data Analytics • Engenharia de Dados • Cloud • Databricks • Python • SQL • Apache Spark • Automação • Inteligência Artificial

---

## 📌 Sobre este repositório

Este é um **repositório educacional**, criado para registrar estudos, exercícios, experimentações e evolução técnica.

Os conteúdos relacionados à Imersão em Engenharia de Dados seguem a proposta educacional da Alura. O objetivo deste repositório não é reproduzir ou comercializar o conteúdo da formação, mas documentar minha prática e aprendizado individual.

---

**Autor:** Abraão Lima
**Área:** Tecnologia da Informação | Dados | Engenharia de Dados | Automação | IA
