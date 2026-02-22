# 🧠 Projeto de Machine Learning — Previsão de Score de Crédito

## 📌 Sobre o Projeto

Este projeto simula um case real de negócio onde um banco fictício precisa automatizar a análise de crédito de seus clientes.

O objetivo foi desenvolver um modelo de **Machine Learning** capaz de prever automaticamente o **score de crédito** de novos clientes com base em seus dados financeiros e comportamentais.

### 🎯 Classes de Score

- 🔴 Poor (Ruim)
- 🟡 Standard (Ok)
- 🟢 Good (Bom)

A solução foi construída utilizando **Python**, com foco em:

- Manipulação e análise de dados
- Preparação e tratamento de variáveis
- Treinamento e comparação de modelos
- Avaliação de desempenho
- Previsão para novos dados

---

## 🚀 Tecnologias Utilizadas

- Python
- Pandas
- Scikit-Learn
- Jupyter Notebook

---

## 📊 Etapas do Projeto

### 1️⃣ Importação e Exploração dos Dados

- Leitura da base `clientes.csv`
- Análise estrutural com `.info()`
- Identificação de colunas categóricas e numéricas
- Entendimento das variáveis relevantes para o modelo

**Principais variáveis analisadas:**

- Salário
- Gastos mensais
- Número de atrasos
- Profissão
- Mix de crédito
- Comportamento de pagamento
- Score de crédito (variável alvo)

---

### 2️⃣ Pré-processamento dos Dados

Como modelos de Machine Learning trabalham apenas com números, foi necessário transformar colunas categóricas em numéricas.

Foi utilizado:

- `LabelEncoder` para codificação de variáveis textuais

**Colunas tratadas:**

- `profissao`
- `mix_credito`
- `comportamento_pagamento`

Também foi realizada a separação entre:

- **X (features)** → variáveis explicativas  
- **y (target)** → `score_credito`

---

### 3️⃣ Treinamento dos Modelos

Foram testados dois algoritmos de classificação:

- 🌳 Random Forest
- 👥 K-Nearest Neighbors (KNN)

**Fluxo aplicado:**

- Criação dos modelos
- Treinamento com dados de treino
- Geração de previsões
- Avaliação com `accuracy_score`

---

### 4️⃣ Avaliação de Performance

Os modelos foram comparados utilizando **acurácia** como métrica principal.

O modelo que apresentou melhor desempenho foi selecionado para realizar previsões em novos clientes.

Essa abordagem demonstra:

✔️ Capacidade de comparação entre algoritmos  
✔️ Tomada de decisão baseada em métricas  
✔️ Mentalidade orientada a dados  

---

### 5️⃣ Previsão para Novos Clientes

Foi utilizada a base `novos_clientes.csv` para simular um cenário real de produção.

**Etapas realizadas:**

- Aplicação do mesmo processo de codificação
- Uso do modelo escolhido
- Geração automática do score de crédito

**Resultado final:**

O modelo retorna a classificação de risco de crédito para cada novo cliente, permitindo que o banco:

- Reduza risco de inadimplência
- Automatize decisões de crédito
- Otimize concessão de limites

---

## 🧠 O que este projeto demonstra

Este projeto evidencia competências importantes para a área de Dados e IA:

✔️ Manipulação e tratamento de dados com Pandas  
✔️ Engenharia de features básica  
✔️ Aplicação prática de algoritmos de classificação  
✔️ Avaliação comparativa de modelos  
✔️ Pensamento orientado a negócio  
✔️ Organização lógica de pipeline de ML  

---

## 📂 Estrutura do Projeto

```bash
📁 Projeto-PythonIA
│
├── clientes.csv
├── novos_clientes.csv
├── inicial.ipynb
└── README.md
```

---

## 🛠️ Como Executar o Projeto Localmente

### 1️⃣ Clone o repositório

```bash
git clone https://github.com/Silos-Antonio/Projeto-PythonIA.git
cd Projeto-PythonIA
```

---

### 2️⃣ Crie um ambiente virtual (Opcional, mas recomendado)

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Mac/Linux

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### 3️⃣ Instale as dependências

```bash
pip install pandas scikit-learn jupyter
```

Ou, caso exista um arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

---

### 4️⃣ Execute o Jupyter Notebook

```bash
jupyter notebook
```

Abra o arquivo:

```
inicial.ipynb
```

Execute as células em ordem para:

- Treinar os modelos
- Comparar desempenho
- Gerar previsões para novos clientes

---

### 5️⃣ Testar com Novos Dados

Você pode editar o arquivo:

```
novos_clientes.csv
```

Adicionar novos registros e executar novamente as células de previsão para simular diferentes cenários de crédito.

---

## 🧪 Requisitos

- Python 3.9+
- Pip instalado
- Jupyter Notebook

---

## 🎯 Possíveis Melhorias Futuras

- Aplicação de validação cruzada (`cross-validation`)
- Ajuste de hiperparâmetros com `GridSearchCV`
- Uso de métricas adicionais (Precision, Recall, F1-Score, Matriz de Confusão)
- Construção de Pipeline com `Pipeline` do Scikit-Learn
- Persistência do modelo com `joblib`
- Deploy do modelo via API usando Flask ou FastAPI

---

## 💡 Insight de Negócio

Mais do que prever um score, este projeto mostra como **Machine Learning pode ser usado como ferramenta estratégica** para apoiar decisões financeiras e reduzir riscos.

Transformar dados em decisão é o que gera valor real.