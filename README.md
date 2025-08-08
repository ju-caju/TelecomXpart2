# 📊 TelecomX – Parte 2: Predição de Evasão de Clientes (Churn)
Este projeto faz parte do desafio final da formação em Data Science.
Seu objetivo é prever a evasão de clientes (churn) com base em variáveis relevantes extraídas e tratadas na Parte 1 do projeto.

## 🎯 Propósito da Análise
O principal objetivo da análise é prever quais clientes estão propensos a abandonar os serviços da empresa (churn), com base em dados históricos.
Através da construção de modelos preditivos, conseguimos identificar padrões de comportamento que influenciam diretamente na decisão dos clientes de continuarem ou não com a empresa.

## 📁 Estrutura do Projeto
bash
Copiar
Editar
telecomx-parte2/
│
├── data/
│   └── dados_tratados.csv       
│
├── notebooks/
│   └── telecomx_modelagem.ipynb 
│
├── outputs/
│   └── graficos/              
│
├── README.md                   

## 🧹 Preparação dos Dados
### ✅ Classificação das variáveis
Categóricas:
customer.gender, account.Contract, account.PaymentMethod, Churn

Numéricas:
account.Charges.Monthly, account.Charges.Total, customer.tenure, Contas_Diarias

## 🔄 Etapas de Tratamento
Remoção de espaços e padronização de strings

Criação de nova variável:

Contas_Diarias = account.Charges.Monthly / 30

Codificação das variáveis categóricas:

Aplicado pd.get_dummies() com drop_first=True

Separação dos dados:

Treino e teste com train_test_split(), utilizando 80% para treino e 20% para teste.

##💡 Modelagem e Justificativas
Foram testados modelos como Regressão Logística e Random Forest.

A escolha final considera performance (Acurácia, Recall, F1-Score) e capacidade de interpretação.

A Random Forest obteve melhores resultados em equilíbrio entre precisão e sensibilidade.

A Reg. Logística foi útil para interpretabilidade dos coeficientes.

## 📊 Exemplos de Gráficos e Insights (EDA)

### ✅ Distribuição de Churn:
Clientes que cancelam o serviço representam uma parcela significativa dos dados, justificando o foco da análise.

### ✅ Boxplots:
Clientes com menor tempo de contrato e cobranças totais mais baixas tendem a sair mais.

### ✅ Gráficos de contagem:
O tipo de contrato (Month-to-month) está fortemente associado ao churn.

(Gráficos estão presentes no notebook telecomx_modelagem.ipynb)

## ▶️ Instruções para Executar o Projeto
Clone o repositório:

bash
Copiar
Editar
git clone https://github.com/ju-caju/telecomxpart2.git
cd telecomxpart2
Instale as bibliotecas necessárias:
(Recomenda-se usar um ambiente virtual)

bash
Copiar
Editar
pip install pandas numpy matplotlib seaborn scikit-learn
Execute o notebook:

Abra o arquivo notebooks/telecomx_modelagem.ipynb no Jupyter Notebook ou Google Colab.

Certifique-se de que o arquivo data/dados_tratados.csv está presente na pasta correta.

## 📌 Observações Finais
Este projeto é uma aplicação prática de tudo que foi aprendido na formação em Data Science, incluindo:

Limpeza e tratamento de dados

Visualização e extração de insights

Criação, validação e comparação de modelos preditivos

Comunicação de resultados através de notebooks e relatórios
