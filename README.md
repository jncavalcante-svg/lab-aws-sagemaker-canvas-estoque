
<img width="1799" height="951" alt="image" src="https://github.com/user-attachments/assets/e42bafea-8050-4991-9e84-111eeeb0dc37" />




1. Visão Geral do Modelo

O modelo foi construído para estimar a quantidade de estoque disponível considerando fatores temporais (data do evento), financeiros (preço) e estruturais (identificação do produto). A plataforma aplicou um processo automatizado de treinamento, validação cruzada e seleção de algoritmo (Quick Build), visando otimizar a métrica principal de Accuracy.

O conjunto de dados utilizado contém:

1.000 registros

4 colunas

Problema caracterizado como previsão categórica com múltiplas classes (3+ category prediction), indicando que a variável QUANTIDADE_ESTOQUE foi tratada como classes discretas, e não como valor contínuo.

2. Métrica Principal de Desempenho
Accuracy (Acurácia)

Valor: 7,563%


Um valor de 7,563% indica que o modelo apresenta baixo poder de generalização no formato atual. Em termos práticos, apenas cerca de 7 em cada 100 previsões coincidem exatamente com a classe real do estoque.

Análise Técnica

Esse resultado sugere:

Alta dispersão da variável-alvo

Classes mal balanceadas

Pouca separabilidade estatística entre os padrões dos dados

Possível inadequação do problema como classificação, quando o mais indicado seria regressão (valor contínuo de estoque)

3. Impacto das Variáveis (Column Impact)

O painel de impacto mostra a importância relativa de cada variável na formação da previsão, medida pelo quanto a alteração dessa variável afeta o resultado final do modelo.

3.1 DATA_EVENTO — 48,203%

É a variável mais influente do modelo.

Interpretação:
A dimensão temporal exerce forte impacto sobre a previsão de estoque, indicando padrões sazonais, picos de consumo ou variações ligadas a datas específicas (eventos, períodos promocionais ou ciclos operacionais).

3.2 PRECO — 29,784%

Segundo fator mais relevante.

Interpretação:
O preço afeta diretamente a dinâmica de saída ou reposição de estoque, influenciando a demanda e, consequentemente, a quantidade disponível.

3.3 ID_PRODUTO — 22,013%

Representa o comportamento específico de cada item.

Interpretação:
Produtos apresentam padrões próprios de consumo e reposição, o que contribui para variações no estoque, porém com menor peso que fatores temporais e financeiros.

4. Análise do Gráfico de Impacto por Data

O gráfico “Impact of DATA_EVENTO on prediction of QUANTIDADE_ESTOQUE” apresenta a variação do impacto da data sobre a previsão ao longo do tempo.

Significado Técnico do Boxplot

Cada caixa representa a distribuição do impacto da variável em um intervalo de data, mostrando:

Mediana do impacto

Dispersão dos valores

Pontos de maior influência positiva ou negativa

Interpretação

Observa-se que:

Algumas datas possuem impacto fortemente positivo, elevando a previsão de estoque

Outras apresentam impacto próximo de zero ou negativo, indicando baixa relevância estatística naquele período

Isso reforça a presença de padrões sazonais e eventos específicos que afetam diretamente a dinâmica do estoque

5. Conclusão Executiva

Apesar de o modelo identificar corretamente os principais fatores explicativos do estoque — especialmente a variável temporal (DATA_EVENTO) — seu desempenho preditivo é tecnicamente baixo no formato atual, conforme indicado pela acurácia de 7,563%.

Isso compromete sua utilização para:

Planejamento automático de reposição

Geração de alertas operacionais confiáveis

Tomada de decisão estratégica baseada em previsão







# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
