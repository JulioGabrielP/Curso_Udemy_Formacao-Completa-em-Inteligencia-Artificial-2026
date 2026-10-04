Mudar de visão: *ctrl* +*shift*+*v*

**Exemplo de classificação**: Asma

Classificação da asma de um paciente: usar machine learning para colocar a asma do paciente em uma das categorias:

- Moderada

- Aguda

- Grave

- Risco de vida

Ou o famoso exemplo do golfe: se jogar golfe ou não, tendo como atributos o tempo, a umidade e o vento, para prever se vou poder jogar ou não.

**Modelo** = Representação daquilo que o algoritmo aprendeu.

## Medir o desempenho de um modelo

**_treino_**: Algoritmo precisa processar dados e criar modelos  -> Feito com parte dos dados históricos usados para criar o modelo  
**_Validação_**: Dados são usados para ajustar o modelo  -> Melhorar perfomance  
**_Teste_**: Dados são usados para avaliar a perfomance do modelo  -> Dados usados para avaliar a perfomance, feito com dados diferentes do texto para evitar enviezamento do modelo.  

*Não existe um modelo que vá ser melhor em tudo no machine learning, cada tipo de problema tem um diferente tipo de algoritmo, com um diferente tipo de parametizalçao que performe melhor*

## Como dividir os dados ?

### Hold-Out
**Separa os dados em treino e teste** em alguma porcentagem (70% treino, 30% teste) -> ambiente de aprendizado

### Validação cruzada
**Divide os dados em vários conjuntos menores**. Supondo que divida os dados em 10 subconjuntos e cada subconjunto tenham o mesmo tamanho, um vai ser usado para treino e todos os outros para teste, depois um dos que era usado para treino passa a fazer parte do grupo de teste, e esse processo é repetido n vezes, sendo n o número de subconjuntos, a ideia é que todo subconjuto seja usado para treino.

### Leave-One-Out
**Tipo o validação cruzada, que treina com todos os conjuntos mas deixa um de fora**, no caso você vai treinando e retirando um dos subconjuntos, volta o que estava fora, retira um e segue pro próximo.

### K-fold
**tipo de validação cruzada**: Divide o conjunto de dados em k (escolhido pelo cientista de dados) e treina o modelo em k-1 subconjuntos e avaliá-lo no subconjunto restante, repete o processo k vezes.

### Subamostragem
**Seleção de uma amostra aleatória de exemplos dos conjuntos de dados para treinamento**. O processo de Rollout é feito várias vezes mas sem controle de quais registros vão ser usados para treino e para teste.

## Generalização VS Super Ajuste VS Sub Ajuste
 * O objetivo de todo classificador é criar um modelo genérico = perfomance semelhante no ambiente de desenvolvimento e no ambiente de produção.

> Super Ajuste : O modelo funciona bem com os dados de treino mas com os dados de teste ou produção ele desempenha mal (Ele decorou as resposta, não aprendeu com elas).   
 Causas: 
 - Tamanho insuficiente do conjunto de dados
 - Complexidade excessiva do modelo
 - Ruído nos dados de treinamento (erros nos dados)
 - Seleção inadequada de atributos
 - Falta da validação cruzada
>Sub Ajuste: O modelo não consegue se ajustar aos dados de treinamento e portanto não consegue generalizar bem para novos dados  
Causas:  
- Modelo muito simples
- Conjunto de dados muito pequenos
- Seleção inadequada de atributos
- Falta de ajuste de hiperparâmetros ?
   