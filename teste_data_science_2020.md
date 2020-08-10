# Teste Data Science Elo7

Esse teste faz parte da terceira etapa do processo seletivo para a vaga no time Data Science do Elo7. O objetivo do teste é avaliar como você desenvolve uma solução completa (em nível de prova de conceito) para um problema de classificação de produtos, que é uma das tarefas que realizamos no nosso dia-a-dia.

## Descrição do Problema

Você deverá construir um classificador de produtos que recebe um conjunto de características de um produto e retorna a categoria dele.

## Dataset

O dataset escolhido para esse teste é composto de uma amostra de dados do Elo7. Você pode obter o dataset através desse [link](https://elo7-datasets.s3.amazonaws.com/data_scientist_position/elo7_recruitment_dataset.csv)

Em resumo, o dataset contém 38.507 registros distribuídos em 5 categorias (`Bebê`, `Bijuterias e Jóias`, `Decoração`, `Lembrancinhas`, `Papel e Cia` e `Outros`). Cada registro corresponde a um clique em um produto a partir de um termo de busca no site. 

Nesse dataset você encontrará as seguintes colunas:

- `product_id` - identificação de produto
- `seller_id` - identificação do vendedor 
- `query` - termo de busca inserido pelo usuário
- `search_page` - número da página que o produto apareceu nos resultados de busca (mín 1 e máx 5)
- `position` - número da posição que o produto apareceu dentro da página de busca (mín 0 e máx 38)
- `title` - título do produto  
- `concatenated_tags` - tags do produto inseridas pelo vendedor (as tags estão concatenadas por espaço)
- `creation_date` - data de criação do produto na plataforma do Elo7
- `price` - preço do produto em reais  
- `weight` - peso em gramas da unidade do produto reportado pelo vendedor
- `express_delivery` - indica se o produto é pronta entrega (1) ou não (0)
- `minimum_quantity` - quantidade de unidades mínima necessária para compra
- `view_counts` - número de cliques no produto nos últimos três meses  
- `order_counts` - número de vezes que o produto foi comprado nos últimos três meses
- `category` - categoria do produto   

Para facilitar a estrutura do teste, nós separamos o desenvolvimento em três etapas: 1) **Análise Exploratória**, 2) **Sistema de Classificação de Produtos** e 3) **Avaliação do Sistema de Classificação**. 

## Parte 1 - Análise Exploratória

Essa etapa é uma das mais importantes de qualquer trabalho de um Cientista de Dados. Antes de executar qualquer algoritmo, nós precisamos primeiro entender o nosso problema. Por isso, gostaríamos que você realizasse uma análise exploratória e indicasse as principais características presentes nos dados. Você tem total liberdade para escolher qualquer ferramenta ou algoritmo nessa etapa.

*Dica*: Para facilitar um pouco o fluxo de informações, recomendamos começar essa etapa explicitando as perguntas que você deseja responder com as análises. Dessa forma, a análise ficará mais estruturada.
    
Use bastante criatividade nessa etapa! Muito provavelmente, essa análise fornecerá ideias para o sistema de classificação de produtos que você precisará desenvolver na etapa seguinte.

## Parte 2 - Sistema de Classificação de Produtos

Implemente um classificador de categorias (a nível de prova de conceito) que categorize da melhor forma os produtos. Escolha as colunas que achar mais apropriadas para a tarefa e procure explicar suas escolhas.

Não vamos indicar nenhum algoritmo ou técnica para executar essa tarefa, porque isso enviesaria a sua solução. Entretanto, gostaríamos que você documentasse todas as decisões tomadas. Não se preocupe em encontrar o melhor algoritmo para resolver o problema. Preferimos que você se preocupe em criar uma boa "história" com os dados, alternando código e o seu raciocínio.

A avaliação dessa etapa vai consistir nesses pontos:
- Estrutura: Código + história
- Conhecimento do problema:
    - Ferramentas de manipulação dos dados
    - Aplicação das técnicas
- **Criatividade** =)

## Parte 3 - Avaliação do Sistema de Classificação

Nessa etapa, gostaríamos que você pensasse sobre que métrica(s) você gostaria de utilizar para avaliar o sistema criado na `Parte 2`.

Essa etapa é muito importante para avaliar e comparar diferentes algoritmos. Podemos utilizar diversas métricas para testar diferentes hipóteses, mas dificilmente teremos uma métrica única para todos os problemas. Que técnica(s) você utilizará para avaliar o seu algoritmo?

*Atenção*: lembre-se de justificar sua escolha da(s) métrica(s) de avaliação.

*Obs*: Novamente, seja **criativo**!

### Observações gerais

Você deve submeter um [jupyter notebook](http://jupyter.org/) com o código desenvolvido por você com a solução desse desafio. Lembre-se de documentar seu código e utilizar células _Markdown_ para explicar **detalhadamente** sua solução. Lembre-se de explicar seu raciocínio e justificar os métodos utilizados por você. Explicite os algoritmos utilizados e as etapas de pré-processamento que você recomenda fazer, justificando o porquê de cada uma das decisões tomadas.

[Aqui](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels) você pode ver uma lista de linguagens compatíveis com o *jupyter* e [aqui](https://ipython.readthedocs.io/en/latest/install/kernel_install.html) algumas instruções que podem auxiliar na instalação da mesma.

Suba um arquivo final `.ipynb`, um `.html` e um `requirements.txt` (gerado pelo comando `pip freeze > requirements.txt`) em seu github pessoal. Deixe o repositório público e nos mande o link por email. Caso tenha utilizado uma linguagem diferente de *Python*, nos **explique** como rodar o seu projeto localmente. Se preferir a utilização do Python, por favor submeta o teste utilizando o Python 3+.

Sinta-se à vontade para fazer o uso de bibliotecas (como o [scikit-learn](http://scikit-learn.org/) e [scipy](https://www.scipy.org/)), mas, novamente, você deve saber explicar o porquê de você aplicar determinado algoritmo para determinada situação.

Utilize a abordagem que se sentir mais á vontade, não é necessário utilizar machine learning.

Não queremos a solução ideal para o problema! Queremos entender sua forma de pensar. =)

**IMPORTANTE**: Seja criativo na resolução do problema! O trabalho de um Cientista de Dados envolve conhecimento técnico, metodologia científica e muita criatividade para abordar problemas complexos. Procure formular uma hipótese, crie o algoritmo de categorização de produtos e encontre uma métrica que teste a sua hipótese.

Boa sorte e qualquer dúvida, pode nos mandar um e-mail!