# AWS Glue Analytics Pipeline
Este projeto demonstra a construção de um pipeline de dados na AWS utilizando AWS Glue, Amazon S3 e Athena, aplicando práticas comuns de engenharia de dados para ingestão, transformação e organização de dados em um Data Lake.

O objetivo é implementar um fluxo de ETL capaz de ingerir dados brutos, transformá-los e disponibilizá-los para consultas analíticas.

# Arquitetura

A arquitetura do pipeline utiliza diferentes serviços da AWS para ingestão, processamento e consulta dos dados.

### Principais componentes utilizados:

**Amazon S3** → armazenamento dos dados no Data Lake
**AWS Glue Crawler** → descoberta automática de esquemas
**AWS Glue Data Catalog** → gerenciamento de metadados
**AWS Glue ETL Jobs** → transformação de dados utilizando PySpark
**AWS Glue Data Quality** → validação da qualidade dos dados
**Amazon Athena** → consultas analíticas utilizando SQL diretamente no Data Lake

# Arquitetura em Camadas do Data Lake

O pipeline segue uma arquitetura de Data Lake em múltiplas camadas, prática comum em projetos de engenharia de dados.

### Camada Bronze

Armazena os dados brutos exatamente como foram recebidos das fontes de origem.

### Camada Silver

Contém os dados tratados e estruturados, após aplicação das transformações necessárias para análise.

Esse modelo permite:

melhor organização dos dados
maior governança
melhor desempenho em consultas analíticas

# Conjunto de Dados

O pipeline processa dados relacionados a vendas, estoque e redes sociais.

Arquivos utilizados no processo de ingestão:

vendas_zoop_bronze.parquet
estoques_zoop_bronze.parquet
redes_sociais_zoop_bronze.parquet

# Pipeline de ETL

O pipeline de processamento segue as seguintes etapas:

1. Upload dos dados brutos para o Amazon S3
2. Descoberta automática do schema utilizando AWS Glue Crawler
3. Registro das tabelas no AWS Glue Data Catalog
4. Criação do pipeline de transformação utilizando AWS Glue Studio
5. Armazenamento dos dados transformados na camada Silver
6. Consulta dos dados utilizando Amazon Athena

# Stack Tecnológica
Amazon S3
AWS Glue
AWS Glue Data Catalog
AWS Glue Data Quality
AWS Glue ETL (Glue Studio)
Amazon Athena
Python
Apache Spark
SQL
