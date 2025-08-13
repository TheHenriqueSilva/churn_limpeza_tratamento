# churn_limpeza_tratamento
Este projeto consiste em um estudo completo de limpeza e tratamento de dados utilizando a biblioteca Pandas, com o objetivo de preparar uma base de dados de telecomunicações para a construção de um modelo de machine learning que preveja o churn de clientes. O código aborda diversas etapas cruciais do pré-processamento de dados, desde a leitura e normalização até o tratamento de variáveis categóricas.

# Principais Etapas do Projeto:
# 1 - Análise Inicial e Normalização de Dados:

Leitura de um arquivo JSON.

Utilização do método pd.json_normalize para converter dados semiestruturados em um DataFrame tabular.

# 2 - Transformação e Limpeza de Dados:

Conversão de tipos de dados (astype), como transformar a coluna de cobrança total em float.

Preenchimento de valores ausentes em colunas numéricas com base em outras colunas.

Remoção de registros com valores vazios ("") na coluna "Churn".

# 3 - Tratamento de Dados Duplicados e Nulos:

Identificação e remoção de linhas duplicadas utilizando df.duplicated() e df.drop_duplicates().

Identificação de valores nulos com df.isna() e df.isna().sum().

Preenchimento de dados nulos na coluna de tempo de serviço, calculando o tempo com base em valores de cobrança.

Remoção de linhas com valores nulos em colunas específicas (dropna).

# 4 - Identificação e Tratamento de Outliers:

Análise de outliers na coluna "cliente.tempo_servico" com a visualização de boxplot usando seaborn.

Cálculo do IQR (Intervalo Interquartil) para identificar valores fora dos limites.

Substituição dos valores considerados outliers ou sua remoção, dependendo da estratégia adotada.

# 5 - Trabalhando com Variáveis Categóricas:

Mapeamento e substituição de valores para variáveis binárias ("sim" / "nao", "masculino" / "feminino").

Utilização de One Hot Encoding através da função pd.get_dummies() para transformar variáveis categóricas nominais em um formato adequado para modelos de machine learning.

Este notebook serve como um guia prático e detalhado das principais técnicas de pré-processamento de dados, mostrando como enfrentar desafios comuns em bases de dados reais para garantir que o conjunto final esteja limpo, consistente e pronto para a fase de modelagem.
