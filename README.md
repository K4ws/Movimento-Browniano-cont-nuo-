# Movimento-Browniano-cont-nuo-

📈 Merton Jump Diffusion: Simulação de Carteira e Análise de Risco
Este repositório contém uma implementação robusta em Python do modelo de Merton Jump Diffusion (MJD). O objetivo é simular o comportamento de uma carteira de ativos da B3 (Bolsa Brasileira), indo além do modelo tradicional de Black-Scholes ao incorporar "saltos" (eventos extremos ou Cisnes Negros).

🚀 Funcionalidades
Coleta Automática: Integração direta com a API yfinance para extração de dados históricos.

Calibração Estatística: Filtro baseado na regra de 3-Sigma para separar a volatilidade do Movimento Browniano dos saltos discretos.

Simulação de Monte Carlo: Geração de milhares de trajetórias correlacionadas via Decomposição de Cholesky.

Métricas de Risco Avançadas:

VaR (Value at Risk) 95%: Perda máxima esperada dentro de um nível de confiança.

CVaR (Conditional VaR) 95%: Perda média esperada em cenários de estresse (além do VaR).


🧠 O Modelo MatemáticoO diferencial deste modelo é a composição do preço em duas partes principais:Componente Difusivo: Oscilação diária normal (ruído de mercado).Componente de Salto: Processo de Poisson que captura choques repentinos.

A dinâmica do preço é regida pela equação diferencial estocástica:$$dS_t = \mu S_t dt + \sigma S_t dW_t + S_t d\left(\sum_{i=1}^{N_t} (J_i - 1)\right)$$Onde:$\mu$ é o drift (retorno esperado).$\sigma$ é a volatilidade do componente contínuo.$dW_t$ é o processo de Wiener (Movimento Browniano).$N_t$ é um processo de Poisson com intensidade $\lambda$.$J_i$ é o tamanho do salto aleatório.


🛠️ Tecnologias UtilizadasBibliotecaUtilidadePython 3.x 
Linguagem base Pandas 
NumPy Processamento de vetores e matrizes 
Yfinance Obtenção de dados do mercado financeiro 
Matplotlib 
Seaborn Visualização de cenários e gráficos de risco
