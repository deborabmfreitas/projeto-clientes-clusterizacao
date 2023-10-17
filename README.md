# Análise de perfil do cliente

<div align="center">

<img src="imgs/clustering.jpg" width="500" alt="img1">

</div>

# Sobre o projeto

Foi criado um problema de negócio fictício utilizando dados públicos do [Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis?select=marketing_campaign.csv).


# Ferramentas e métodos

- Python
- Principais frameworks/bibliotecas: Pandas, Matplotlib, Seaborn e Sci-kit learn
- Jupyter Notebook (projeto) e VSCode (README)
- Git e GitHub
- Análise exploratória de dados (EDA) e features engineering 
- Método **Elbow**
- Algoritmo de machine learning **Kmeans**.


# Problema de negócio

Uma loja de departamentos nova pertencente à empresa Walmart está enfrentando dificuldades para segmentar seus clientes de acordo com suas personalidades,  algo que dificulta o desenvolvimento de campanhas de marketing eficazes e personalizadas. Sendo assim, a empresa deseja **identificar padrões comportamentais e preferências** entre seus clientes, a fim de criar segmentos de mercado mais precisos para suas campanhas.


# Abordagem estratégica

O projeto de análise de personalidade de clientes busca agrupá-los em diferentes segmentos com base em suas personalidades. Isso permite que a empresa desenvolva campanhas de marketing mais personalizadas e direcionadas, atendendo às necessidades e preferências de cada segmento. Do ponto de vista de um cientista de dados, é possível oferecer soluções utilizando **algoritmos de clusterização**.

# Descrição dos dados

Coluna | Descrição
-------| --------
ID | Identificador do cliente
Year_Birth | Ano de nascimento do cliente
Education| Nível de escolaridade do cliente
Marital_Status | Estado civil do cliente
Income | Renda familiar anual do cliente
Kidhome | Número de crianças na casa do cliente
Teenhome | Número de adolescentes na casa do cliente
Dt_Customer | Data de inscrição do cliente na empresa
Recency | Número de dias desde a última compra do cliente
Complain| Reclamações do cliente; 1: reclamou nos últimos 2 anos, 0: não reclamou
MntWines | Valor gasto em vinho nos últimos 2 anos
MntFruits | Valor gasto com frutas nos últimos 2 anos
MntMeatProducts | Valor gasto com carne nos últimos 2 anos
MntFishProducts | Valor gasto com pescados nos últimos 2 anos
MntSweetProducts | Valor gasto com doces nos últimos 2 anos
MntGoldProds | Valor gasto em ouro nos últimos 2 anos
AcceptedCmp1 | 1: cliente aceitou a oferta de promoção na 1ª campanha, 0: não aceitou
AcceptedCmp2 | 1: cliente aceitou a oferta de promoção na 2ª campanha, 0: não aceitou
AcceptedCmp3 | 1: cliente aceitou a oferta de promoção na 3ª campanha, 0: não aceitou
AcceptedCmp4 | 1: cliente aceitou a oferta de promoção na 4ª campanha, 0: não aceitou
AcceptedCmp5 | 1: cliente aceitou a oferta de promoção na 1ª campanha, 0: não aceitoupromoção
Response | 1: cliente aceitou a oferta de promoção na última campanha, 0: não aceitou
NumDealsPurchases | Nº de compras feitas com desconto
NumCatalogPurchases | Nº de compras feitas por catálogo
NumStorePurchases | Nº de compras feitas diretamente nas lojas
NumWebPurchases | Nº de compras feitas através do site da empresa
NumWebVisitsMonth | Nº de visitas ao site da empresa no último mês

# Etapas gerais do projeto

A princípio, os dados foram tratados, analisados e foi feita a etapa detalhada de EDA em conjunto com a de Feature engineering. Exemplos de algumas features derivadas são as colunas `TotalAmountSpent` e `TotalPurchases`, correspondentes ao gasto de compras e ao ticket médio, respectivamente.

 Após os processos anteriores, foi feita uma alocação de pesos nas variáveis mais importantes e o método para a seleção de clusters foi o **Elbow**. As etapas futuras podem incluir a aplicação do `silhouette_score` na próxima versão do projeto, para que sejam investigadas novas possibilidades de clusters. Por fim, o algoritmo de clusterização utilizado foi o **K-Means**.
 
 Os clientes foram segmentados em 4 clusters: `Cluster 0`, `Cluster 1`, `Cluster 2` e `Cluster 3`.


# Perfil dos clientes

De maneira geral, os clientes são, em média, pessoas mais velhas, com um intervalo entre 52 a 58 anos.

## Cluster 0

Em geral, foi visto que os clientes do cluster 0 são os que gastam menos, possuem o menor ticket médio, aproveitam bem as promoções, possuem a menor renda com exceção a alguns outliers, costumam visitar mais o site que os demais, apesar de comprarem mais nas lojas físicas e possuem menos dias desde a última compra. Por fim, são os clientes mais recentes da loja e possuem mais filhos que os clientes dos clusters 1 e 2.

## Cluster 1

Clientes que mais gastam, quase o dobro do cluster 2, que ocupa a segunda posição. Possuem o maior ticket médio, compram mais produtos a preço cheio do que em promoção, apresentam a maior renda, compram mais por catálogos e não costumam visitar tanto o site da loja quanto os demais. Por fim, são os que menos possuem filhos e são os clientes mais antigos da loja. **Podem ser considerados clientes de alto valor para o negócio**.

## Cluster 2

Clientes costumam gastar algum dinheiro, embora o valor caia pela metade se comparado aos clientes do cluster 1. Possuem um ticket médio intermediário e aproveitam pouco as promoções, sendo o dobro do cluster 1 e quase metade se comparado aos clusters 3 e 0. Além disso, apresentam a segunda maior renda. Tamném são clientes antigos e os que menos possuem filhos após o cluster 1.

## Cluster 3

Os clientes costumam gastar pouco, possuem um ticket médio maior apenas que os clientes do cluster 0, aproveitam bem as promoções, ocupando o primeiro lugar por muito pouco. Além disso, possuem uma renda menor, ficando próxima dos clientes do cluster 0. São também clientes que mais visitam o site, mais possuem filhos e os que estão a mais tempo sem comprar na loja, podendo ser investigada a possibilidade de churn ser maior nesse grupo.

## Considerações

Com base nessas análises, é possível auxiliar a equipe de marketing na tomada de decisão.


Clique [aqui](https://github.com/deborabmfreitas/projeto-clientes-clusterizacao/blob/main/clustering-project.ipynb) para acompanhar o projeto em mais detalhes.
