# Analise_Dados_Climaticos

## Análise de Dados Climáticos de Delhi (2014-2017)
Este repositório contém uma análise detalhada dos dados climáticos históricos da cidade de Delhi, Índia, para o período de 2014 a 2017. O objetivo é identificar padrões e construir modelos preditivos para a temperatura média. Abaixo está um resumo das ferramentas utilizadas, o processo seguido e as principais análises realizadas.

### Ferramentas Utilizadas
* **Linguagem de Programação:** Python

* **Bibliotecas:**

**Pandas:** Para manipulação e análise de dados.

**Matplotlib:** Para visualização dos dados.

**Statsmodels:** Para análise estatística e testes de estacionaridade.

**pmdarima (AutoARIMA):** Para ajuste e previsão de modelos ARIMA.

**StatsForecast:** Para implementação do modelo Naive.

### Processo de Análise

**Carregamento e Visualização dos Dados**

* Carregamos o dataset contendo variáveis climáticas, como temperatura média, umidade, velocidade do vento e pressão média.
* Utilizamos gráficos de linha para visualizar as séries temporais de cada variável.

**Decomposição da Série Temporal**

* Analisamos a tendência, sazonalidade e ruído na série temporal da temperatura média.

**Análise de Estacionaridade**

* Aplicamos o teste de Dickey-Fuller aumentado (ADF) para verificar a estacionaridade da série temporal.
* A série original não foi estacionária, mas a transformação logarítmica resultou em uma série estacionária.

**Cálculo da Média Móvel**

* Calculamos e plotamos a média móvel de 30 dias para suavizar a série e evidenciar as tendências de longo prazo.

**Análise de ACF e PACF**

* Plotamos as funções de autocorrelação (ACF) e autocorrelação parcial (PACF) para identificar a estrutura de autocorrelação da série.

**Modelagem Preditiva**

* Modelo Naive: Utilizado como baseline com um WMAPE de 3.97%.
* Modelo SARIMAX: Ajustado com parâmetros ARIMA (1, 1, 1) apresentou um WMAPE de 3.77% e um MAPE de 3.89%.

### Resultados e Conclusões
* A análise revelou padrões sazo nais e uma tendência geral na temperatura média de Delhi.
* A transformação logarítmica foi eficaz para tornar a série temporal estacionária, permitindo a modelagem preditiva.
* O modelo SARIMAX superou o modelo Naive em precisão de previsão, com menores erros percentuais.
* As análises destacam a importância de considerar sazonalidade e tendência ao modelar séries temporais climáticas.

**Este repositório fornece um ponto de partida robusto para a análise e previsão de dados climáticos, com uma abordagem prática para a modelagem de séries temporais. O código e os resultados detalhados estão disponíveis para referência e expansão em projetos futuros.**

Para mais detalhes, consulte os arquivos de código e documentação neste repositório.
