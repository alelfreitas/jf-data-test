# Avaliação para Engenharia de Dados/Analise de Dados

## Requisitos

1.	Infraestrutura
    - Utilize uma VM Linux configurada no VirtualBox.
    - Configure os seguintes containers utilizando Docker:
    - SQL Server
    - MongoDB
    - PySpark
    - Airflow
2.	Dataset
    - Baixe o dataset sobre o  conjunto de dados públicos de comércio eletrônico brasileiro
no Kaggle (https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce). 
3.	Arquitetura de Dados
    - Implemente uma arquitetura em camadas, composta por:
    - Raw Layer: Armazene os dados brutos do dataset.
    - Trusted Layer: Realize limpeza e transformação dos dados assim como o Data Quality
    - Delivered Layer: Dados prontos para análise e modelagem.
4.	Modelagem Relacional
    - Utilize uma ferramenta de modelagem (como MySQL Workbench, ER/Studio, etc.) para criar um Modelo Entidade-Relacionamento (MER) do dataset.
    - A partir do MER, crie a base de dados física no SQL Server. Esta base deve suportar operações transacionais do dia a dia dos produtos. 
5.	Modelagem Multidimensional
    - Desenvolva um modelo multidimensional (esquema estrela ou floco de neve) para análise OLAP dos dados de produtos.
    - Crie as tabelas de fato e dimensões no SQL Server e carregue os dados transformados.
    - Consultas a Realizar utilizando PySpark SQL:
    - Análise de Desempenho de Vendas: Total de vendas por produto, categoria, região e período (diário, semanal, mensal, anual).
    - Análise de Tendências: Tendências de vendas e demanda ao longo do tempo.
    - Análise de Clientes: Segmentação de clientes por frequência de compra e valor gasto.
    - Análise de Comportamento de Compras por Região: Quais são as regiões com maior volume de vendas e quais as categorias de produtos que são mais vendidos em cada região?
    - Análise de Frequência de Compras:Qual é a frequência média de compras dos clientes e quais fatores influenciam a frequência de compras?
6.	Forecast
    - Desenvolva e aplique um modelo de previsão (forecast) sobre os dados diários dos produtos.
    - Utilize PySpark para implementar e treinar o modelo de forecast.
    - Armazene os resultados das previsões em um banco de dados NoSQL (MongoDB) para consultas rápidas e escaláveis.
    - Consultas NoSQL:
    - Consulta de Previsões Diárias: Previsões de vendas diárias para cada produto.
    - Análise de Acurácia: Comparação entre previsões e dados reais para calcular a acurácia do modelo.
    - Armazenamento de Resultados de Forecasts: Estrutura de armazenamento dos resultados das previsões, incluindo dados históricos e comparações de desempenho.
7.	Orquestração com Airflow
    - Utilize o Airflow para orquestrar o fluxo de dados e tarefas. Crie DAGs (Directed Acyclic Graphs) para automatizar os seguintes processos:
    - Ingestão de dados brutos do dataset.
    - Transformação e carregamento dos dados nas camadas Raw, Trusted e Delivered.
    - Treinamento e execução do modelo de forecast com PySpark.
    - Armazenamento dos resultados das previsões no MongoDB.
    - Atualização dos dashboards no Power BI (use APIs ou scripts para automação, se possível).
8.	Visualização de Dados
    - Utilize o Power BI para criar dashboards e relatórios que comprovem a eficiência do modelo preditivo.
    - Os dashboards devem incluir:
    - Visualização das previsões diárias.
    - Comparação entre dados reais e previstos.
    - Insights sobre tendências e anomalias.
    - Análise de acurácia do modelo de forecast.
    - Identificação de outliers nas previsões e nos dados reais.
9.	Discussão sobre CRISP-DM
    - Discorra sobre o que é o CRISP-DM (Cross Industry Standard Process for Data Mining).
    - Descreva cada uma das etapas do processo: Compreensão do Negócio, Compreensão dos Dados, Preparação dos Dados, Modelagem, Avaliação e Implementação.
    - Explique a importância do CRISP-DM em projetos de dados e como ele pode ajudar a estruturar e orientar o desenvolvimento de soluções de análise de dados.
## Entregáveis

- Arquivos
- Imagem da VM com todo o projeto funcional. 
- Documentação
- Descreva detalhadamente cada etapa do processo, desde a configuração da infraestrutura até a implementação dos modelos e visualizações.
- Inclua capturas de tela e descrições dos scripts e configurações utilizadas.
- Scripts e Configurações
- Scripts Docker para configuração dos containers.
- Scripts SQL para criação e manipulação da base de dados no SQL Server.
- Código PySpark para a implementação do modelo de forecast.
- Estrutura do documento NoSQL e código para armazenamento no MongoDB.
- DAGs do Airflow para orquestração dos processos.
- Modelos e Diagramas
- MER da base relacional.
- Modelo multidimensional (esquema estrela ou floco de neve).
- Diagrama da estrutura do documento NoSQL.
- Arquivos Power BI com os dashboards e relatórios.
- Ensaio sobre CRISP-DM
- Documento explicando o CRISP-DM, suas etapas e importância em projetos de dados.

## Critérios de Avaliação

- Leveling: Não é preciso realizar o teste completo. Faça apenas o que conseguir.
- Accuracy: Precisão dos modelos preditivos e eficácia das transformações e consultas.
- Efficiency: Eficiência na execução dos scripts e queries.
- Clarity: Clareza e organização da documentação e do código.
- Visualization: Qualidade e relevância das visualizações em Power BI.
- Insight: Compreensão e explicação do CRISP-DM e sua aplicação em projetos de dados. 
