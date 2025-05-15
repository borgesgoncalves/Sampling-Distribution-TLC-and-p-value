# Análise Estatística, Distribuições Amostrais e Teorema do Limite Central

Este repositório contém o desenvolvimento de uma atividade prática explorando conceitos fundamentais da estatística inferencial, incluindo distribuições amostrais, o Teorema do Limite Central (TLC) e o cálculo do p-value.

## Visão Geral dos Exercícios

O projeto aborda quatro exercícios distintos, cada um focando em um aspecto importante da análise estatística:

* **A: Distribuição Amostral e Distribuição de Amostragem**: Exploração da diferença entre a distribuição de uma amostra individual e a distribuição das médias de múltiplas amostras retiradas de uma população.
* **B: Teorema do Limite Central**: Demonstração empírica do Teorema do Limite Central aplicado à distribuição Gama, observando como a distribuição das médias amostrais se aproxima de uma normal com o aumento do tamanho da amostra.
* **C: Valor-p**: Implementação passo a passo do cálculo do p-value para um evento específico, ilustrando o processo de avaliação da significância estatística.
* **D: Teste de Hipóteses**: Investigação da taxa de falso negativos ao calcular p-values para amostras de uma distribuição Gaussiana em relação a outra, simulando um cenário de teste de hipóteses.

## Detalhes dos Conceitos Utilizados

A seguir, uma explicação mais detalhada dos conceitos estatísticos aplicados em cada exercício:

### A: Sample distribution and Sampling distribution

* **Conceitos:**
  * A distribuição Gaussiana (ou normal) é uma das distribuições de probabilidade mais comuns, caracterizada por sua forma de sino simétrica em torno da média. A forma e a posição de uma distribuição normal são completamente determinadas por dois parâmetros: Média (μ) e Desvio Padrão (σ). Com base na distribuição da população ou na distribuição de amostragem, é possivel calcular a probabilidade de observar certos eventos.
  * A inferência estatística é o processo de tirar conclusões sobre uma população inteira com base em informações obtidas de uma amostra dessa população.
  * Seleção da Amostra: A forma como a amostra é selecionada é fundamental para garantir que ela seja representativa da população. Existem dois tipos principais de técnicas de amostragem
  * Amostragem Probabilística (Aleatória): Cada membro da população tem uma chance conhecida e não nula de ser selecionado para a amostra.
  * Amostragem Aleatória Simples: Todos os membros têm a mesma probabilidade de serem selecionados. É como um sorteio.
  * É importante avaliar a confiabilidade das inferências feitas. Isso envolve considerar o erro amostral, que é a diferença entre a estatística amostral e o parâmetro populacional devido à aleatoriedade da amostragem. O erro amostral é a diferença entre uma estatística calculada a partir de uma amostra e o verdadeiro parâmetro da população da qual a amostra foi retirada
  * A margem de erro (ME) é uma medida comum do erro amostral.

  
* **Sample Distribution (Distribuição Amostral):**
    * **Conceito:** A distribuição amostral representa a distribuição dos valores individuais observados em uma única amostra retirada da população. Ela reflete a variabilidade dos dados dentro dessa amostra específica.
    * **Demonstração:** Você irá visualizar a distribuição dos dados de uma das amostras coletadas da sua população Gaussiana artificial.

* **Sampling Distribution (Distribuição de Amostragem):**
    * **Conceito:** A distribuição de amostragem é a distribuição das estatísticas de amostras (como a média amostral) calculadas a partir de *muitas* amostras independentes do mesmo tamanho retiradas da mesma população. O Teorema do Limite Central (abordado no Exercício B) descreve uma propriedade importante dessa distribuição para a média amostral.
    * **Demonstração:** Você irá gerar várias amostras da sua população Gaussiana, calcular a média de cada amostra e, em seguida, visualizar a distribuição dessas médias. Essa distribuição das médias é a distribuição de amostragem da média.

* **Avaliações de Probabilidade de Possíveis Eventos:**
    * **Conceito:**  Por exemplo, qual a probabilidade de uma amostra ter uma média acima de um determinado valor?
    * **Aplicação:** Você aplicará os conhecimentos sobre a distribuição Gaussiana (para a população) e possivelmente a distribuição de amostragem da média para calcular essas probabilidades.

### B: TLC (Teorema do Limite Central)

* **Teorema do Limite Central (TLC):**
    * **Conceito:** Um dos teoremas mais importantes da estatística. Ele afirma que, independentemente da forma da distribuição da população original, a distribuição da *média amostral* de um número suficientemente grande de amostras independentes e identicamente distribuídas (i.i.d.) se aproximará de uma distribuição normal. Essa aproximação melhora à medida que o tamanho da amostra aumenta.
    * **Condições:** Para o TLC se aplicar de forma eficaz, as amostras devem ser aleatórias, independentes e o tamanho da amostra geralmente precisa ser "suficientemente grande" (embora o que constitui "suficientemente grande" possa variar dependendo da forma da distribuição original).

* **Função de Distribuição Gama:**
    * **Conceito:** A distribuição Gama é uma distribuição de probabilidade contínua com dois parâmetros (forma e taxa ou escala). Ela é frequentemente usada para modelar tempos de espera, taxas de falha e outros fenômenos com assimetria positiva.
    * **Aplicação:** Neste exercício, você aplicará o TLC a amostras retiradas de uma população com distribuição Gama. Como a distribuição Gama geralmente não é normal, este exercício demonstrará como a distribuição das médias amostrais se torna aproximadamente normal à medida que o tamanho da amostra aumenta.

* **Avaliação com Diferentes Tamanhos de Amostra (n=10, ...):**
    * **Demonstração:** Você irá gerar distribuições de médias amostrais para diferentes tamanhos de amostra (começando em 10 e aumentando). Ao visualizar essas distribuições, você poderá observar visualmente a convergência para uma distribuição normal conforme o tamanho da amostra cresce, ilustrando o TLC em ação.

### C: P-value (Valor-p)

* **P-value (Valor-p):**
    * **Conceito:** O p-value é a probabilidade de obter resultados tão extremos (ou mais extremos) quanto os resultados observados em sua amostra, *assumindo que a hipótese nula seja verdadeira*. Ele é usado em testes de hipóteses para determinar a significância estatística dos resultados. Um p-value pequeno (geralmente ≤ 0.05) sugere que os dados observados são improváveis sob a hipótese nula, levando à sua rejeição.
    * **Passo a Passo do Cálculo:** O programa demonstrará as etapas para calcular o p-value para um evento específico. Isso geralmente envolve:
        1.  **Formular a hipótese nula e a hipótese alternativa.**
        2.  **Escolher uma estatística de teste apropriada** (baseada nos dados e na hipótese).
        3.  **Calcular o valor da estatística de teste** a partir dos dados da amostra.
        4.  **Determinar a distribuição da estatística de teste sob a hipótese nula.**
        5.  **Calcular a probabilidade (o p-value) de observar um valor da estatística de teste tão extremo ou mais extremo do que o calculado, assumindo que a hipótese nula é verdadeira.**

* **Figuras para Cada Passo:** A inclusão de figuras para cada etapa do cálculo do p-value ajudará a visualizar o processo, como a distribuição nula e a área correspondente ao p-value.

### D: P-value (Taxa de Falso Negativos)

* **Duas Gaussianas:**
    * **Conceito:** Você criará duas populações artificiais com distribuições Gaussianas, possivelmente com médias e/ou desvios padrões diferentes.

* **Sorteio de Sequências e Cálculo do P-value:**
    * **Processo:** Para cada uma das 100 sequências de três valores sorteadas da primeira Gaussiana (a "azul"), você realizará um teste de hipóteses (implícito ou explícito) em relação à segunda Gaussiana (a "vermelha"). O p-value será calculado para cada sequência, indicando a probabilidade de observar essa sequência (ou algo mais extremo) se ela realmente viesse da distribuição vermelha.
    * **Seta Vermelha:** A "seta vermelha" que indica a partir de qual amostra o p-value é calculado é crucial para entender qual dado está sendo testado em relação à distribuição de referência.

* **Taxa de Falso Negativos:**
    * **Conceito:** Em um teste de hipóteses, um falso negativo (erro do tipo II) ocorre quando não rejeitamos a hipótese nula quando ela é, na verdade, falsa. No contexto deste exercício, se assumirmos que as amostras da Gaussiana azul *são* diferentes da Gaussiana vermelha (nossa "verdade"), um falso negativo ocorreria quando o p-value calculado (ao testar se a amostra azul poderia ter vindo da vermelha) for alto o suficiente para *não* rejeitar essa possibilidade (geralmente p-value > 0.05).
    * **Cálculo:** Você calculará a proporção das 100 sequências para as quais o p-value foi maior que 5% (0.05). Essa proporção representa a taxa de falso negativos na sua simulação.

## Como Usar este Repositório

[Esta seção explicará como executar seus scripts, quais bibliotecas são necessárias e como interpretar os resultados. Inclua instruções sobre como configurar o ambiente, executar os códigos e visualizar as saídas (gráficos, valores de p, taxa de falso negativos, etc.).]

## Contribuições

[Se você planeja permitir contribuições, explique como as pessoas podem participar.]

## Licença

[Adicione a licença sob a qual seu código está distribuído.]

---

Este README fornece uma base sólida para explicar os conceitos estatísticos envolvidos em sua atividade. Ao completar as seções sobre "Como Usar este Repositório", você terá um guia completo para quem quiser entender e executar seu trabalho. Boa sorte com a finalização da sua atividade! Se tiver mais dúvidas, pode perguntar!