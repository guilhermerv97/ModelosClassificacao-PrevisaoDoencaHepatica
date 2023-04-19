# Comparação entre Modelos de Classsificação para Previsão de Ocorrência de Doença Hepática.

Neste estudo de caso, feito para o curso Big Data Real-Time Analytics com Python e Spark da Data Science Academy, temos o uso de Machine Learning para, a partir de dados históricos, prever se uma pessoa terá uma doença hepática ou não. Assim, a variável alvo é categórica (possui não possui doença hepática), de modo que este se trata de um problema de Classificação. Aqui é feita análise exploratória, tratamento dos dados e preparação e treinamento de 5 algoritmos diferentes: Regressão Logística, Decision Tree, Random Forest, K-Nearest Neighbors e Support Vector Machines (SVM). Os modelos foram comparados, e, a partir de sua performance, foi escolhido um melhor modelo pra previsão de novos dados. A partir da comparação dos parâmetros, o modelo Random Forest apresentou melhor performance, e ele foi usado para a previsão de ocorrência de doença hepática em novos dados hipotéticos.

## Análise Exploratória de Dados
Na análise exploratória, foi feita uma separação entre variáveis categóricas e numéricas, para que ambos os tipos de variáveis pudessem ser avaliados separadamente. A exploração foi feita através de gráficos de distribuição de frequência e de estudos das relações entre as variáveis.
Além disso, foi feita uma análise para identificação e remoção de dados duplicados e ausentes.

## Pré-Processamento de Dados
No pré-processamento, uma das variáveis foi removida, por apresentar elevada correlação com outra variável preditora, o que pode indicar colinearidade, ou seja, duas variáveis carregando a mesma informação, o que pode tornar o modelo tendencioso.
Os dados foram divididos em dados de treino e teste, usando a proporção de 75/25, respectivamente.
Por fim, é necessário preparar os dados para os modelos. Para isso, as variáveis categóricas foram balanceadas usando over-sampling, de modo a evitar diferença nas frequências e impedir o modelo de aprender igualmente sobre todas. Já as variáveis numéricas foram padronizadas, impedindo que variáveis estejam em ordens de grandeza diferentes, e, portanto, influenciem os modelos de forma diferente. Todos os processamentos feitos nos dados de treino também foram feitos nos dados de teste, uma vez que são necessários para obtenção de resultados válidos nos modelos.

## Modelos de Machine Learning
Foram selecionados 5 algoritmos diferentes para a análise de Classificação: Regressão Logística, Decision Tree, Random Forest, K-Nearest Neighbors e Support Vector Machines (SVM). Em cada modelo foi estudada a otimização de hiperparâmetros e a importância de cada variável para o modelo. Para a comparação entre os modelos, foram usados os seguintes parâmetros: acurácia, score AUC, e score ROC. Os resultados foram guardados em um dataframe, onde foi possível perceber que, para este conjunto de dados e com os hiperparâmetros utilizados, o modelo com maior acurácia e maior score AUC foi o modelo Random Forest. A partir dele, foi feita uma previsão utilizando dados hipotéticos, que passaram pelos mesmos processamentos que os dados de treino e teste. Nesta análise foi previsto que o paciente não deve apresentar doença hepática.
