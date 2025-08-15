# Análise de Evasão de Clientes (Churn) - Telecom X

![Análise de Dados](https://img.shields.io/badge/Análise_de_Dados-Python-blue.svg)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen.svg)

---

## 📖 Índice

- [1. Visão Geral do Projeto](#1-visão-geral-do-projeto)
- [2. Fonte dos Dados](#2-fonte-dos-dados)
- [3. Ferramentas e Bibliotecas](#3-ferramentas-e-bibliotecas)
- [4. Estrutura do Projeto](#4-estrutura-do-projeto)
- [5. Como Executar o Projeto](#5-como-executar-o-projeto)
- [6. Metodologia da Análise](#6-metodologia-da-análise)
- [7. Principais Conclusões e Recomendações](#7-principais-conclusões-e-recomendações)
- [8. Autor](#8-autor)

---

## **1. Visão Geral do Projeto**

Este projeto consiste em uma Análise Exploratória de Dados (EDA) sobre a evasão de clientes (churn) em uma empresa fictícia de telecomunicações, a **Telecom X**. O objetivo principal é identificar os principais fatores e perfis de clientes que possuem maior probabilidade de cancelar seus serviços. A análise serve como base para a tomada de decisões estratégicas, visando a criação de ações para aumentar a retenção e a fidelidade dos clientes.

---

## **2. Fonte dos Dados**

Os dados foram obtidos a partir de um arquivo JSON disponibilizado em uma URL. Este arquivo contém informações demográficas dos clientes, detalhes dos serviços contratados (telefone, internet, etc.), informações da conta (tipo de contrato, método de pagamento) e o status de evasão de cada cliente.

- **URL da API de Dados:** `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/refs/heads/main/TelecomX_Data.json`

---

## **3. Ferramentas e Bibliotecas**

As seguintes ferramentas e bibliotecas Python foram utilizadas para a realização deste projeto:

- **Python 3.x**
- **Pandas**: Para manipulação e tratamento dos dados.
- **Plotly Express**: Para a criação de visualizações de dados interativas.
- **Jupyter Notebook / VS Code**: Como ambiente de desenvolvimento para a análise.
- **Kaleido**: Para exportar os gráficos do Plotly como imagens estáticas.
- **IPython**: Para exibição de imagens e outros elementos ricos no notebook.
- **nbformat**: Dependência para renderização de notebooks.

---

## **4. Estrutura do Projeto**

O repositório está organizado da seguinte forma:

- `TelecomX_BR.ipynb`: O notebook principal contendo todo o código e a análise, desde a extração dos dados até o relatório final.
- `/imagens/`: Pasta contendo os gráficos gerados e salvos como arquivos `.png` durante a análise.
- `README.md`: Este arquivo, que fornece uma visão geral e instruções sobre o projeto.

---

## **5. Como Executar o Projeto**

Para executar este projeto em seu ambiente local, siga os passos abaixo:

**Pré-requisitos:**

- Python 3.x instalado.
- `pip` (gerenciador de pacotes do Python).

**Passos:**

1. **Clone o repositório:**

   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   cd seu-repositorio
   ```

2. **Instale todas as dependências:**
   É recomendado criar um ambiente virtual. Após criá-lo, instale todas as bibliotecas necessárias com um único comando:

   ```bash
   pip install pandas plotly kaleido==0.2.1 nbformat jupyterlab
   ```

3. **Execute o Jupyter Notebook:**
   ```bash
   jupyter lab
   ```
   No seu navegador, abra o arquivo `TelecomX_BR.ipynb` e execute as células de código em sequência.

---

## **6. Metodologia da Análise**

A análise foi conduzida seguindo um processo estruturado de ETL (Extração, Transformação e Carga) e EDA (Análise Exploratória de Dados).

- **Extração e Carga**: Os dados foram carregados diretamente da URL do arquivo JSON para um DataFrame do Pandas.
- **Tratamento e Transformação**:
  - **Normalização**: A estrutura aninhada do JSON foi "achatada" para um formato tabular.
  - **Limpeza**: Foram corrigidos tipos de dados (ex: `faturamento_total`), tratados valores ausentes e padronizados nomes de colunas.
  - **Engenharia de Features**: Foi criada a coluna `faturamento_diario` para enriquecer a análise.
  - **Padronização**: Dados categóricos foram convertidos para formato numérico (0/1) e traduzidos para o português, garantindo consistência e clareza.
- **Análise Exploratória de Dados (EDA)**:
  - **Análise Descritiva**: Calculamos métricas estatísticas para entender a distribuição geral dos dados.
  - **Análise Gráfica**: Utilizamos gráficos de rosca, barras agrupadas e box plots para visualizar a relação entre a variável `evasao` e outras características dos clientes.

---

## **7. Principais Conclusões e Recomendações**

A análise revelou padrões claros que ajudam a identificar os clientes com maior risco de evasão.

### **Perfil de Risco**

> O cliente com maior probabilidade de cancelar o serviço é aquele que está há **poucos meses na empresa**, possui um **contrato mensal**, utiliza o serviço de **Fibra Ótica**, paga suas contas via **cheque eletrônico** e **não possui serviços de suporte** adicionais.

### **Recomendações Estratégicas**

1.  **Revisar a Estratégia de Contratos**: Criar campanhas agressivas para migrar clientes do plano mensal para contratos de 1 ou 2 anos, oferecendo descontos ou benefícios claros.
2.  **Investigar o Serviço de Fibra Ótica**: A alta evasão neste segmento precisa ser investigada. A empresa deve analisar se o problema está no preço, na qualidade/estabilidade do serviço ou na concorrência.
3.  **Incentivar Pagamentos Automáticos**: Incentivar ativamente a migração para métodos de pagamento automáticos, que estão associados a clientes mais fiéis.
4.  **Criar Ofertas de Serviços Agregados**: Oferecer "pacotes de fidelidade" ou descontos na contratação de serviços como `suporte_tecnico` e `seguranca_online` para clientes de alto risco.
5.  **Foco nos Primeiros Meses**: Criar um programa de _onboarding_ e acompanhamento para os primeiros 3 a 6 meses de vida do cliente, garantindo uma boa experiência inicial e fortalecendo o relacionamento.

---

## **8. Autor**

**Matheus Nascimento Leite**

- [LinkedIn](https://www.linkedin.com/in/matheusnleite)
- [GitHub](https://github.com/matheusnleite)
