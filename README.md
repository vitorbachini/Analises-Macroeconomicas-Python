# Análises Macroeconômicas em Python

Estudo das relações entre SELIC, IPCA e Taxa de Câmbio (USD/BRL) utilizando dados reais do Banco Central do Brasil (2010–2025), foi baseado em Análises Estatísticas, Análises Gráficos e Modelos Vetoriais Autorregressivos (VAR).

📊 Objetivo
Compreender as dinâmicas e transmissões macroeconômicas entre taxa de juros, inflação e câmbio, aplicando metodologia econométrica rigorosa (testes de estacionariedade, VAR, diagnóstico de resíduos, função impulso–resposta).

📌 Principais Etapas
ETL: Extração, transformação e carregamento dos dados extraídos da API do Banco Central.

Exploração: Visualização das séries e estatísticas descritivas.

Estacionariedade: Testes ADF e KPSS; diferenciação das séries.

Seleção de Ordem: Critérios AIC, BIC, HQIC para escolha de defasagem (lags).

Modelo VAR: Ajuste de regressão multivariada com defasagens.

Diagnóstico: Análise de resíduos (Ljung-Box, Jarque-Bera, estabilidade).

Impulso–Resposta: Mapeamento de transmissões de choques (12 meses).

📈 Resultados Principais

- A Taxa Selic é uma ferramenta importante do nosso Sistema Financeiro, o governo a utiliza para tentar conter a inflação e alta do Dólar, isso fica claro através das análises gráficas e estatísticas realizadas no estudo. Durante os diversos ciclos da economia brasileira no período ela se mostrou bem volátil, tendo como valor mínimo 1,9% e valor máximo 14,9%.
  
- O IPCA se mostrou uma variável estruturalmente alta e muito sensível às políticas econômicas internas e externas. Durante o período analisado a sua média se manteve sempre acima da meta com valor de ~ 5,8% e chegou a atingir o valor de ~ 12,13% no período pós-pandemia.
  
- A Taxa de Câmbio foi a variável que apresentou menor desvio, desde 2011 seu valor vem crescendo ao longo dos anos, o que reflete a desconfiança do mercado externo nas políticas econômicas adotadas no brasil. Seu pico foi de R$ 6,19.

- Para o modelo VAR, foi escolhido um período de defasagem de um mês, sugerido pelo critério BIC (mais conservador). O modelo se mostrou estável e sugere que, sim, a taxa Selic e o IPCA se relacionam positivimante durante o período, ou seja, o aumento de uma variável tende a provocar o aumento da outra, vale ressaltar que os testes realizados para a variável Dólar se mostraram estatisticamente fracos. Além disso, para os dados selecionados o modelo apresentou forte autocorrelação para a variável Selic, o que pode atrapalhar a dinâmica do modelo.
