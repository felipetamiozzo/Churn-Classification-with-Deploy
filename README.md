# Deploy Classification - Machine Learning

Este repositório contém um projeto de **classificação** utilizando Machine Learning e um ambiente virtual gerenciado pelo **Conda**.

---

## 📌 Descrição

### 📊 Business Understanding
A empresa fictícia analisada neste projeto é uma provedora de serviços de telecomunicações, oferecendo telefonia fixa e Internet residencial para **7.043 clientes** no estado da Califórnia, durante o terceiro trimestre (Q3).

O objetivo principal é compreender os fatores que levam à saída de clientes (**churn**), identificar aqueles com maior risco e propor estratégias de retenção eficazes. A redução da rotatividade de clientes é essencial para:
- Minimizar impacto na receita recorrente;
- Reduzir custos de aquisição de novos clientes;
- Priorizar clientes com alto **Customer Lifetime Value (CLTV)**.

**Perguntas-chave:**
- Quais características mais contribuem para o churn?
- Quais perfis de clientes são mais propensos a cancelar os serviços?
- Quais estratégias podem ser implementadas para reter clientes, especialmente os mais valiosos?

### 📁 Data Understanding
O conjunto de dados utilizado contém **7.043 observações** e **33 variáveis**, organizadas em diferentes categorias:

#### 🔹 Informações Gerais
- **CustomerID**: Identificação única do cliente.
- **Localização**: Estado, cidade, código postal e coordenadas geográficas.

#### 🔹 Características Demográficas
- **Gender**: Gênero (Masculino/Feminino).
- **Senior Citizen**: Indica se tem 65 anos ou mais.
- **Partner** e **Dependents**: Indica se tem parceiro(a) ou dependentes.

#### 🔹 Serviços Contratados
- **Tenure Months**: Tempo (em meses) como cliente da empresa.
- **Phone Service** e **Multiple Lines**: Uso de telefonia fixa.
- **Internet Service**: Tipo de conexão (DSL, Fibra Óptica, Cabo ou Nenhum).
- **Serviços Adicionais**: Segurança online, backup, suporte técnico, streaming, entre outros.

#### 🔹 Informações Contratuais e Financeiras
- **Contract**: Tipo de contrato (Mensal, Anual, Bienal).
- **Payment Method**: Método de pagamento (Cartão, Débito, Cheque).
- **Monthly Charge** e **Total Charges**: Valores pagos pelos serviços.

#### 🔹 Indicadores de Churn
- **Churn Label**: Cliente cancelou ou não.
- **Churn Score**: Probabilidade de cancelamento (0 a 100).
- **CLTV**: Valor vitalício do cliente.
- **Churn Reason**: Motivo do cancelamento.

---

## 🔍 Exploratory Data Analysis (EDA)

- **Distribuição de Churn**
- **Churn vs Gênero, Idade, Tempo de Permanência**
- **Churn vs Método de Pagamento**
- **Heatmap de Correlação**
- **Distribuição de Variáveis Categóricas vs Churn**

---

## 🔬 Feature Importance

- **Seleção das variáveis mais relevantes para o modelo**
- **Comparação de diferentes algoritmos de Machine Learning**

---

## 🤖 Modelagem e Avaliação

### **Pipelines e Modelos**
- **Algoritmos**: Random Forest, Regressão Logística, LightGBM
- **Grid Search** para otimização de hiperparâmetros
- **Matriz de Confusão (Heatmap)**
- **Curva ROC e AUC**
- **Comparação dos valores reais vs previstos**

---

## 🚀 Deployment

### Aplicação com Streamlit

O projeto conta com uma interface interativa desenvolvida com **Streamlit**, permitindo que os usuários façam upload de um arquivo CSV contendo dados de clientes e obtenham previsões de churn. O aplicativo:

1. Carrega um modelo treinado.
2. Permite o upload de arquivos CSV.
3. Exibe as previsões de churn e probabilidades.
4. Oferece a opção de download dos resultados.

**Nota:** O deploy foi realizado apenas **localmente**, sem disponibilização em ambiente público.

### 📌 Tecnologias Utilizadas

- **Python 3.11**
- **Machine Learning Models**: RandomForest, LogisticRegression, LightGBM
- **Framework de Interface**: Streamlit
- **Ambiente Virtual**: Conda
- **Bibliotecas Principais**:
  - `lightgbm`, `matplotlib`, `numpy`, `pandas`, `pickle`, `seaborn`, `sklearn`, `streamlit`, `warnings`

### 📂 Estrutura do Projeto
```
│── customer_churn        # Arquivo .csv com os dados
│── deploy_classification # Diretório do projeto
│── app.py                # Script principal da API (Streamlit)
│── models/model.pkl      # Modelo treinado
│── requirements.txt      # Lista de dependências
│── README.md             # Documentação do projeto
```

---

## ⚙️ Como Configurar o Ambiente

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/seu-repositorio.git
   cd seu-repositorio
   ```

2. **Crie e ative um ambiente Conda**:
   ```bash
   conda create --name meu_ambiente python=3.11
   conda activate meu_ambiente
   ```

3. **Instale as dependências**:
   ```bash
   pip install -r requirements.txt
   ```

---

## 🎯 Executando a Aplicação

Para iniciar a aplicação localmente, utilize:
```bash
streamlit run app.py
```

