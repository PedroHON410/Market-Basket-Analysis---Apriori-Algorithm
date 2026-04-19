# 🛒 Market Basket Analysis - Apriori Algorithm
Este projeto utiliza o algoritmo Apriori para realizar uma análise de cestas de compras (Market Basket Analysis), identificando padrões de associação entre produtos comprados frequentemente em conjunto.

O objetivo é extrair regras do tipo "quem compra o Produto A, também costuma comprar o Produto B", permitindo estratégias de marketing mais eficazes, como cross-selling e otimização de layout de prateleiras.

## 📊 Sobre o Algoritmo
O algoritmo Apriori é uma técnica de mineração de dados utilizada para encontrar conjuntos de itens frequentes em bases de dados transacionais. Ele utiliza as seguintes métricas principais para validar as associações:

* Suporte (Support): Indica a frequência com que um conjunto de itens aparece nas transações.

* Confiança (Confidence): Mede a probabilidade de um item B ser comprado dado que o item A foi adquirido.

* Lift: Indica a força da regra, mostrando o quanto a presença do item A aumenta a probabilidade de venda do item B em comparação com a venda de B de forma independente.

## 🛠️ Tecnologias Utilizadas
```
Linguagem: Python.

Biblioteca Principal: mlxtend (Machine Learning Extensions), apriori e association_rules.

Manipulação de Dados: Pandas.
```
## ⚙️ Fluxo do Projeto
* Carregamento dos Dados: Leitura da base de dados de transações (ex: mercado.csv ou similar).

* Pré-processamento: Transformação dos dados para o formato binário (One-Hot Encoding), onde cada linha representa uma transação e cada coluna um produto (True/False).

* Geração de Itemsets Frequentes: Aplicação do algoritmo Apriori com um suporte mínimo definido.

* Extração de Regras: Geração de regras de associação baseadas em métricas de confiança e lift.

## 📈 Exemplo de Aplicação
Ao analisar os dados, o modelo consegue identificar relações como:

{Pão, Manteiga} -> {Leite}: Clientes que compram pão e manteiga têm 80% de chance de também levar leite.
