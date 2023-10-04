## Desafio 04 - Data Cleaning e Data Wrangling de um dataset de E-commerce

### Contexto
Uma empresa do ramo de e-commerce contratou você para levantar os indicadores de recência, frequência e ticket médio (RFM) dos seus clientes. A saber RFM:
- R (Recency): Tempo que o cliente realizou a última compra (em dias)
- F (Frequency): Quantidade de compras realizadas pelo cliente
- M (Monetary): Valor do ticket médio gasto pelo cliente
onde ticket médio = média do total gasto por pedido para cada cliente.

Para isso, será realizado um processo de Data Cleaning e Data Wrangling de uma base de dados (data.csv) e gerado um output em formato csv, para posterior modelagem do novo database.

### Sobre os dados
O database contém informações de compras de um e-commerce em 37 países. É composto por 8 colunas, sendo elas:
- CustomerID: Código de identificação do cliente
- Description: Descrição do produto
- InvoiceNO: Código da fatura
- StockCode: Código de estoque do produto
- Quantity: Quantidade do produto
- InvoiceDate: Data do faturamento (compra)
- UnitPrice: Preço unitário do produto
- Country: País da compra

### Objetivo
- Definir um novo dataset em formato .csv, com tratamento de dados e constando as seguintes colunas:
  - CustomerID: Código do cliente
  - R: Recência, que é a diferença em dias da última compra do cliente e da última compra disponível no conjunto de dados que calcularam previamente.
  - F: Frequência, ou seja, a quantidade de compras feitas pelo cliente.
  - M: Ticket médio, ou seja, a média das compras feitas pelo cliente.
- Realizar a plotagem de gráficos para visualização de métricas gerais de venda.

### Procedimentos
Serão realizados os seguinte procedimentos para alcançar o objetivo:
- Análise dos dados iniciais em relação a granularidade, constância e distribuição;
- Tratamento de dados nulos, caso existam, por meio de drop de colunas ou input de dados;
- Tratamento de outliers;
  - Foi informado anteriormente que a faixa de preço e quantidades usuais giram em torno de 10000 unidades e 5000 de valor unitário. Isto será considerado na correção dos outliers caso sejam identificados.
- Tratamento de dados duplicados;
- Tratamento de tipificação de colunas;
- Cálculos e colunas RFM, por meio de operações arítméticas;
- Plotagem de gráficos para visualização de variáveis:
  - Top 10 países com maior valor em vendas
  - Top 10 produtos mais vendidos
  - Valor de venda total por mês
  - Valor de venda total por mês e por país (top 10)

### Ferramentas a serem utilizadas e documentação
Seguem abaixo as ferramentas / bibliotecas a serem utilizadas, com suas respectivas documentações:
- Pandas: https://pandas.pydata.org/docs/reference/index.html
- Numpy: https://numpy.org/doc/stable/reference/
- ydata_profiling: https://docs.profiling.ydata.ai/4.5/
- Plotly: https://plotly.com/python-api-reference/
- Matplolib: https://matplotlib.org/stable/api/index.html
