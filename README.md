# criminalidade_sp
Repositório do terceiro MVP da minha pós graduação de Ciência de Dados e Analytics na PUC Rio

## Checklist do MVP:
Resolvi responder as perguntas uma a uma, para dar uma visão clara dos pontos de atenção do projeto.

### Definição do Problema

Objetivo: entender e descrever claramente o problema que está sendo resolvido.

**Qual é a descrição do problema?** Compreender como se comportam os registros de boletins de ocorrência no estado de São Paulo
**Você tem premissas ou hipóteses sobre o problema? Quais?** Não tenho
**Que restrições ou condições foram impostas para selecionar os dados?** São dados reais, necessitam de muito tratamento, fora que são dados muito volumosos.
**Descreva o seu dataset (atributos, imagens, anotações, etc).** Os dados estão descritos no notebook

### Preparação de Dados

Objetivo: realizar operações de preparação dos dados.

**Separe o dataset entre treino e teste (e validação, se aplicável).** Separado em T e T+1
**Faz sentido utilizar um método de validação cruzada? Justifique se não utilizar.** Não, foi realizada uma clusterização
**Verifique quais operações de transformação de dados (como normalização e padronização, transformação de imagens em tensores) são mais apropriadas para o seu problema e salve visões diferentes do seu dataset para posterior avaliação dos modelos.** Realizado
**Refine a quantidade de atributos disponíveis, realizando o processo de feature selection de forma adequada.** Realizado de forma quase "orgânica", sem detalhamento dos motivos de escolha (pelo tempo).

### Modelagem e treinamento:

Objetivo: construir modelos para resolver o problema em questão.

**Selecione os algoritmos mais indicados para o problema e dataset escolhidos, justificando as suas escolhas.** Escolhi K-Means, por ser um clássico (como baseline) e GMM, que não se mostrou melhor que o K-Means
**Há algum ajuste inicial para os hiperparâmetros?** Apenas ajustes do tamanho de K
**O modelo foi devidamente treinado? Foi observado problema de underfitting?** Sim, houve underfitting, com muita sobreposição dos centroides
**É possível otimizar os hiperparâmetros de algum dos modelos? Se sim, faça-o, justificando todas as escolhas.** Não foi possível, acredito que precisava de mais trabalho de feature engineering
**Há algum método avançado ou mais complexo que possa ser avaliado?** Sim, mas ainda acredito que com mais trabalho de feature engineering teria chegado a resultados melhores
**Posso criar um comitê de modelos diferentes para o problema (ensembles)?** Provavelmente sim, mas não sei se os resultados seriam tão diferentes sem um trabalho mais robusto de feature engineering

### Avaliação de Resultados:

Objetivo: analisar o desempenho dos modelos gerados em dados não vistos (com a base de teste)

**Selecione as métricas de avaliação condizentes com o problema, justificando.** Métricas corretas e aderentes selecionadas. 
**Treine o modelo escolhido com toda a base de treino, e teste-o com a base de teste.** Realizados em T e T+1.
**Os resultados fazem sentido?** Sim, os padrões dos clusters se mantiveram.
**Foi observado algum problema de overfitting?** Mais de underfitting.
**Compare os resultados de diferentes modelos.** Foram comparados.
**Descreva a melhor solução encontrada, justificando.** Escolhi a menos pior, seria necessário mais trabalho para garantir um modelo mais robusto.
