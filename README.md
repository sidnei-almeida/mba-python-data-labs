<h1 align="center">MBA Python Data Labs</h1>

<p align="center">
  <strong>Python · Pandas · Matplotlib · Google Colab</strong><br />
  <em>Datasets e laboratórios práticos para aulas de análise de dados.</em>
</p>

<p align="center">
  <a href="https://github.com/sidnei-almeida/mba-python-data-labs"><strong>Ver no GitHub</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Pandas-análise-150458?logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/Matplotlib-visualização-11557c" alt="Matplotlib" />
  <img src="https://img.shields.io/badge/Google-Colab-F9AB00?logo=googlecolab&logoColor=white" alt="Google Colab" />
  <img src="https://img.shields.io/badge/Uso-educacional-blue" alt="Uso educacional" />
</p>

---

## O que é este repositório

Base centralizada de **arquivos CSV** e **notebooks** usados nos laboratórios práticos de Python e análise de dados. A ideia é simples: os alunos abrem o notebook no Colab e carregam os dados direto do GitHub, sem precisar baixar arquivos manualmente nem montar pastas no Drive.

> **Público:** iniciantes em Python e Data Science, em turmas que trabalham com Pandas, limpeza de dados e primeiras visualizações.

---

## Objetivo

| Meta | Descrição |
|------|-----------|
| **Centralizar dados** | Um único lugar para os CSVs das aulas |
| **Facilitar o Colab** | Leitura via URL pública (`raw.githubusercontent.com`) |
| **Apoiar o lab** | Notebooks alinhados ao ritmo da aula, com exercícios práticos |
| **Reduzir fricção** | Menos tempo configurando ambiente, mais tempo analisando dados |

---

## Estrutura do repositório

Estrutura alvo (pastas podem ser reorganizadas conforme novos labs forem adicionados):

```text
.
├── data/
│   └── dirty_cafe_sales.csv
├── notebooks/
│   └── lab_01_exploracao_limpeza_pandas.ipynb
└── README.md
```

**Estado atual:** o Lab 01 (versão 2) está na raiz como `lab_01_exploracao_limpeza_pandas_v2.ipynb`; o dataset já está em `data/`.

---

## Datasets disponíveis

| Arquivo | Tema | Uso no lab | Status |
|---------|------|------------|--------|
| `data/dirty_cafe_sales.csv` | Vendas de cafeteria com dados sujos | Lab 01 — exploração, limpeza e tipos com Pandas | Disponível |

O arquivo contém colunas como item, quantidade, valor, forma de pagamento, local e data, com problemas típicos de mundo real: `UNKNOWN`, `ERROR`, ausências e tipos inconsistentes — ideais para praticar `.replace()`, `.dropna()`, `.fillna()`, `pd.to_numeric()` e `pd.to_datetime()`.

---

## Como usar no Google Colab

### 1. Abrir o notebook

Use um link neste formato (ajuste o caminho se o notebook estiver em `notebooks/`):

```text
https://colab.research.google.com/github/sidnei-almeida/mba-python-data-labs/blob/main/lab_01_exploracao_limpeza_pandas_v2.ipynb
```

Depois: **Arquivo → Salvar uma cópia no Drive**, para que cada aluno tenha sua própria cópia editável.

### 2. Carregar o CSV com Pandas

Substitua `SEU_USUARIO` e `NOME_DO_REPO` apenas se estiver usando um fork; neste repositório oficial:

```python
import pandas as pd

url = "https://raw.githubusercontent.com/sidnei-almeida/mba-python-data-labs/main/data/dirty_cafe_sales.csv"

df = pd.read_csv(url)
df.head()
```

A URL `raw.githubusercontent.com` aponta para o arquivo bruto no branch `main` — é o padrão recomendado no Colab.

### 3. Executar em ordem

Rode as células de cima para baixo. Muitos exercícios usam `assert` para validar o resultado; pular células costuma gerar erros difíceis de depurar no início.

---

## Laboratórios

| Lab | Conteúdo | Status |
|-----|----------|--------|
| **Lab 01** — Exploração e limpeza de dados com Pandas | Leitura de CSV, `.info()`, valores ausentes, limpeza e primeiro `.groupby()` | Disponível (`lab_01_exploracao_limpeza_pandas_v2.ipynb`) |
| **Lab 02** — Análise exploratória | Estatísticas descritivas e perguntas sobre os dados | Planejado |
| **Lab 03** — Visualização com Matplotlib | Gráficos para comunicar achados | Planejado |
| **Lab 04** — Mini-projeto guiado | Integração leve de limpeza, análise e visualização | Planejado |

---

## Para quem é este material

- Alunos **iniciantes** em Python que já viram variáveis, listas e funções básicas
- Quem está aprendendo **Pandas** na prática (não só na teoria)
- Estudantes de **análise de dados** e cursos com foco em negócios / MBA
- Turmas que usam **Google Colab** como ambiente principal da aula

Não é necessário instalar Python localmente para seguir os labs, desde que o notebook e o CSV sejam carregados como descrito acima.

---

## Boas práticas para os alunos

| Prática | Por quê |
|---------|---------|
| Abrir o notebook pelo **Colab** (link do GitHub) | Ambiente já configurado com Pandas e Matplotlib |
| **Salvar uma cópia no Drive** | Evita sobrescrever o notebook original e perde progresso |
| Executar as células **em ordem** | Variáveis e exercícios dependem das etapas anteriores |
| **Ler os comentários** nas células | Explicam o “porquê”, não só o “como” |
| Tentar os **exercícios** antes de olhar a solução | Fixa o raciocínio; os `assert` ajudam a corrigir na hora |

---

## Contribuição e evolução

Novos datasets entram em `data/`; novos notebooks em `notebooks/` (ou na raiz, até a pasta existir). Ao adicionar um CSV, atualize a tabela **Datasets disponíveis** neste README.

---

## Autoria

**Criado por Sidnei Alves de Almeida** — [@sidnei-almeida](https://github.com/sidnei-almeida)

Material desenvolvido para apoio em **aulas práticas de Python e análise de dados**, com foco em Pandas, exploração de dados e primeiros passos em visualização.
