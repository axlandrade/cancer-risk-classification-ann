# Cancer Risk Classification using Artificial Neural Network (ANN)

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Model](https://img.shields.io/badge/ML-ANN%20MLPClassifier-orange.svg)
![K-Fold](https://img.shields.io/badge/Validation-10--Fold-yellow.svg)

Este repositório contém o desenvolvimento completo do trabalho prático da disciplina de **Inteligência Artificial** do mestrado em Modelagem Matemática e Computacional, da UFRRJ.  
O objetivo é construir um modelo supervisionado capaz de **classificar o risco de câncer** utilizando uma **Rede Neural Artificial (ANN)** com **validação cruzada k-fold** e obter **acurácia ≥ 0.70**.

---

## Objetivos do Projeto

1. Realizar **limpeza, normalização e preparação dos dados** do arquivo  
   `classificacao_risco_cancer_varios_valores.csv`
2. Construir e treinar um modelo baseado em **MLPClassifier (Scikit-Learn)**
3. Utilizar **validação cruzada estratificada (k-fold)** para avaliar o desempenho
4. Garantir acurácia média **≥ 0.70**
5. Gerar documentação acadêmica em **LaTeX** e um **Jupyter Notebook** replicável

---

## Estrutura do Repositório

```
/
├── data/
│   └── classificacao_risco_cancer_varios_valores.csv
├── notebook/
│   └── Trabalho_IA_classificacao_risco_cancer.ipynb
├── report/
│   └── relatorio.tex   (a ser gerado)
├── requirements.txt
└── README.md
```

---

## Metodologia

### 1. Pré-processamento
- Remoção da variável de identificação (`Patient Id`)
- Substituição de strings que representam valores ausentes
- Imputação:
  - Numéricos → **mediana**
  - Categóricos → **mais frequente**
- One-hot encoding para variáveis categóricas
- Padronização dos atributos numéricos

### 2. Modelo
Foi utilizada uma **Rede Neural Multicamada (MLPClassifier)** com:

- `hidden_layer_sizes=(50, 30)`
- `activation="relu"`
- `solver="adam"`
- `max_iter=500`
- Pipeline completo integrando preprocessamento + ANN

### 3. Avaliação
A avaliação foi feita com:

- **Validação cruzada estratificada**
- `k = 10 folds`
- Métrica: **Acurácia**
- Requisito do trabalho: **acurácia ≥ 0.70**

---

## Como Executar (Localmente)

### 1.1. Instalar dependências

```bash
pip install -r requirements.txt
```

### 1.2. Rodar o notebook

```bash
jupyter notebook notebook/Trabalho_IA_classificacao_risco_cancer.ipynb
```

---

## Google Colab

(Link a ser adicionado)

------

## Resultados

O notebook contém:

- Tabela com acurácia por fold
- Acurácia média
- Discussão dos resultados
- Possíveis melhorias e experimentos adicionais

---

## Relatório Acadêmico

O relatório em LaTeX será disponibilizado em:

```
/report/relatorio.tex
```

---

## Autor

**Axl Andrade**  
Mestrado em Inteligência Artificial – Projeto de Classificação de Risco de Câncer

**Rodrigo Vitorino**  
Mestrado em Inteligência Artificial – Projeto de Classificação de Risco de Câncer

---

## Licença

Este projeto está licenciado sob a licença MIT.
