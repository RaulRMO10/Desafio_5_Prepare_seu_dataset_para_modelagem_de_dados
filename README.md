# Projeto de Limpeza e Organização de Dados

Este repositório contém o código e os processos utilizados para realizar a limpeza e organização de um conjunto de dados, preparando-o para modelagem preditiva. A limpeza e organização de dados são etapas cruciais para garantir a precisão e a robustez dos modelos de aprendizado de máquina.

## Etapas Realizadas

### 1. Inspeção Inicial dos Dados
- **Leitura do dataset:** Carregamento dos dados brutos para iniciar a análise.
- **Distribuição dos dados:** Uso de métodos estatísticos descritivos (`describe`) para obter uma visão geral.
- **Tipo dos dados:** Verificação dos tipos de dados em cada coluna para identificar inconsistências.

### 2. Tratamento de Valores Faltantes
- **Valores nulos:** Identificação de valores nulos com `isna` e `sum`.
- **Remoção de nulos:** Utilização da função `dropna` para remover observações com valores nulos.

### 3. Validação de Preços Unitários e Quantidades
- **Filtros de validação:** Verificação e remoção de preços e quantidades que sejam nulos ou menores que zero.

### 4. Verificação de Linhas Duplicadas
- **Identificação e remoção:** Utilização das funções `duplicated` e `drop_duplicates` para remover linhas duplicadas.

### 5. Correção de Tipos de Dados
- **Ajustes de tipo:** Correção dos tipos de dados para garantir consistência, especialmente para `CustomerID` e `InvoiceDate`.

### 6. Tratamento de Outliers
- **Identificação:** Visualização e remoção de outliers extremos, considerando valores de quantidade superiores a 10.000 e preços unitários maiores que 5.000.

### 7. Criação de Coluna Adicional
- **Coluna TotalPrice:** Criação de uma nova coluna calculada a partir de `Quantity` e `UnitPrice`.

### 8. Cálculo da Última Data de Compra
- **Última compra:** Utilização da função `max()` para determinar a data mais recente de compra no dataset.

### 9. Visualização dos Dados
- **Top 10 países por valor em vendas:** Preparação e plotagem de gráficos para visualizar os principais países em termos de vendas.
- **Top 10 produtos mais vendidos:** Identificação e visualização dos produtos mais vendidos.
- **Vendas totais por mês:** Análise mensal do valor de vendas.
- **Vendas mensais por país:** Visualização das vendas mensais por país, focando nos top 10 países.

### 10. Cálculo do RFM
- **Recência, Frequência e Valor Monetário:** Agrupamento dos dados por cliente e cálculo dos indicadores RFM:
  - **Recency (R):** Diferença em dias da última compra do cliente e da última compra disponível no conjunto de dados.
  - **Frequency (F):** Quantidade de compras realizadas pelo cliente.
  - **Monetary (M):** Ticket médio, ou seja, a média das compras feitas pelo cliente.

## Importância

Dominar a limpeza e organização de dados é fundamental para:
- **Modelos Precisos:** Geração de modelos mais precisos e confiáveis.
- **Eficiência:** Redução do tempo gasto em depuração e retrabalho.
- **Insights Valiosos:** Extração de insights valiosos e acionáveis dos dados.
- **Valor para o Negócio:** Melhoria da qualidade das previsões e recomendações baseadas em dados.
