# Análise Exploratória de Dados de Aluguel de Imóveis

Este repositório contém um notebook Jupyter (ou Google Colab) que realiza uma análise exploratória de dados de aluguéis de imóveis. O objetivo principal é entender as características da base de dados, limpar e tratar valores nulos, remover registros irrelevantes, criar novas colunas e gerar filtros específicos para análise.

## Sumário do Projeto

O projeto aborda as seguintes etapas:

1.  **Importação de Dados**: Carregamento da base de dados de aluguéis a partir de uma URL.
2.  **Conhecendo a Base de Dados**: Exploração inicial da estrutura dos dados, tipos de colunas, dimensões e primeiras/últimas linhas.
3.  **Análise Exploratória**: Cálculo do valor médio de aluguel por tipo de imóvel e visualização desses dados.
4.  **Limpeza de Dados**: Identificação e remoção de imóveis comerciais para focar em propriedades residenciais.
5.  **Tratamento de Valores Nulos**: Preenchimento de valores ausentes com zero nas colunas `Valor`, `Condominio` e `IPTU`.
6.  **Remoção de Registros Inconsistentes**: Exclusão de registros onde o `Valor` ou `Condominio` era igual a zero.
7.  **Filtros Específicos**: Criação de DataFrames filtrados com base em critérios como número de quartos, valor do aluguel e área.
8.  **Criação de Novas Colunas**: Geração de colunas como `Valor_por_mes`, `Valor_por_ano`, `Descricao` e `Possui_suite` para enriquecer a análise.
9.  **Exportação de Dados**: Salvamento dos DataFrames processados em arquivos CSV.

## Base de Dados

O dataset utilizado é `aluguel.csv`, obtido do seguinte link:
[https://raw.githubusercontent.com/alura-cursos/pandas-conhecendo-a-biblioteca/main/base-de-dados/aluguel.csv](https://raw.githubusercontent.com/alura-cursos/pandas-conhecendo-a-biblioteca/main/base-de-dados/aluguel.csv)

## Como Executar o Notebook

Você pode executar este notebook no Google Colab ou em seu ambiente local (por exemplo, Jupyter Notebook):

### Google Colab

1.  Abra o notebook no Google Colab.
2.  Execute as células sequencialmente.

### Ambiente Local (Jupyter Notebook/Lab)

1.  Certifique-se de ter Python e as bibliotecas necessárias instaladas (`pandas`, `matplotlib`, `seaborn`).
2.  Faça o download do notebook para sua máquina local.
3.  Abra um terminal, navegue até o diretório onde o notebook foi salvo e execute `jupyter notebook`.
4.  Abra o arquivo `.ipynb` e execute as células.

## Dependências

-   `pandas`
-   `matplotlib` (para visualizações)
-   `seaborn` (para visualizações)

Para instalar as dependências, você pode usar pip:

```bash
pip install pandas matplotlib seaborn
```

## Resultados e Insights (Exemplos)

Alguns insights obtidos da análise incluem:

*   A distribuição de tipos de imóveis na base, com **Apartamentos** sendo o tipo mais comum (aproximadamente 84%).
*   O valor médio de aluguel varia significativamente entre os diferentes tipos de imóveis.
*   Foram criados DataFrames específicos para apartamentos com 1 quarto e aluguel menor que R$1200, e apartamentos com 2 ou mais quartos, aluguel menor que R$3000 e área maior que 70m².

## Arquivos Gerados

Durante a execução do notebook, os seguintes arquivos CSV são gerados:

-   `dados_apartamentos.csv`: Contém apenas os registros de apartamentos, com valores nulos tratados e registros inconsistentes removidos.
-   `filtro_1.csv`: Apartamentos com 1 quarto e aluguel menor que 1200.
-   `filtro_2.csv`: Apartamentos com pelo menos 2 quartos, aluguel menor que 3000 e área maior que 70m².
-   `dados_completos_dev.csv`: O dataset original com tratamento de nulos e as novas colunas (`Valor_por_mes`, `Valor_por_ano`, `Descricao`, `Possui_suite`).

## Autor

[Seu Nome/Nome de Usuário do GitHub]
