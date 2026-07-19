# Classificação de Falhas em Máquinas Industriais

> Projeto de Machine Learning desenvolvido para prever falhas em máquinas industriais a partir de dados operacionais e de sensores. O projeto contempla todas as etapas de um fluxo de Ciência de Dados, incluindo análise exploratória, engenharia de atributos, pré-processamento, balanceamento de dados, treinamento de modelos e avaliação dos resultados.

-----
## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)

  ---------

## Divisão das partes do projeto
O projeto foi dividido em seis etapas principais:

### Parte 1 – Análise Exploratória dos Dados (EDA)

Nesta etapa foi realizada a análise exploratória do conjunto de dados, utilizando gráficos de boxplot, histogramas e matriz de correlação de Pearson. Também foram analisados os dados faltantes, a presença de valores duplicados, a distribuição das variáveis e a comparação entre média e mediana para auxiliar na definição da estratégia de imputação.

### Parte 2 – Engenharia de Atributos (Feature Engineering)

Nesta etapa foram criadas três novas variáveis a partir das características originais do conjunto de dados, com o objetivo de fornecer informações adicionais aos modelos de Machine Learning:

- **potencia:** produto entre a velocidade de rotação e o torque.
- **delta_temperatura:** diferença entre a temperatura do processo e a temperatura do ar.
- **desgaste_torque:** produto entre o desgaste da ferramenta e o torq

### Parte 3 –  Divisão, preparação das colunas e  Balanceamento dos Dados

Nesta etapa foi realizado o pré-processamento dos dados para o treinamento dos modelos de Machine Learning, contemplando as seguintes etapas:

1. Separação das variáveis preditoras (**X**) e da variável alvo (**y**), seguida da divisão dos dados em conjuntos de treino e teste.

2. Imputação dos valores faltantes utilizando a **média** ou a **mediana**, conforme a distribuição de cada variável.

3. Codificação da variável categórica **tipo** por meio de variáveis dummies.

4. Balanceamento da base de treinamento utilizando a técnica **SMOTE (Synthetic Minority Over-sampling Technique)**.

### Parte 4 – Escalonamento das Variáveis (StandardScaler)

Nesta etapa foi aplicado o **StandardScaler** às variáveis preditoras utilizadas pelo modelo **K-Nearest Neighbors (KNN)**, uma vez que esse algoritmo é sensível à escala das variáveis.

Para a **Árvore de Decisão**, foram mantidos os dados originais, pois esse algoritmo não requer escalonamento das variáveis.

### Parte 5 – KNN e Árvore de Decisão

Nesta etapa foram treinados os modelos **K-Nearest Neighbors (KNN)** e **Árvore de Decisão**, comparando diferentes configurações de hiperparâmetros. A avaliação foi realizada utilizando a métrica de **acurácia** nos conjuntos de treino e teste.

### Parte 6 – Avaliação dos Modelos

Nesta etapa foi realizada a avaliação dos modelos, comparando seus desempenhos e analisando os principais casos de erro. Ao final, foram propostas melhorias e sugestões para trabalhos futuros.

# Informações Adicionais

Este projeto utiliza o conjunto de dados **manutencao_preditiva.csv**.

A descrição de cada variável, bem como informações complementares sobre o conjunto de dados, estão disponíveis no documento **Anotações do Departamento de Engenharia.pdf**


