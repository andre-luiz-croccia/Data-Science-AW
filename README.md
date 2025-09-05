# Data-Science-AW
📊 Previsão de Demanda e Análise Temporal — Checkpoint 5 | Data Science
🧠 Objetivo
Este projeto tem como finalidade responder ao Checkpoint 5 da trilha de Data Science, por meio da construção de um pipeline preditivo capaz de estimar a demanda futura de produtos em diferentes lojas. A abordagem combina técnicas de regressão supervisionada, séries temporais e modelagem estatística para gerar previsões confiáveis e apoiar decisões estratégicas baseadas em dados.

🛠️ Etapas do Projeto
1. Previsão de Vendas por Produto e Loja
- Os dados foram agrupados por produto e id_loja, formando séries temporais mensais.
- Foram aplicados três modelos de regressão: Random Forest, XGBoost e LightGBM.
- Em casos com histórico insuficiente, foi utilizada uma média móvel como alternativa.
- As previsões foram organizadas em formato tabular, permitindo comparações diretas entre os modelos.
2. Avaliação de Desempenho dos Modelos
- Foram calculadas métricas de avaliação: MAE, RMSE e R², usando os últimos 3 meses como teste.
- Essa etapa permitiu identificar o modelo mais adequado para cada combinação de produto e loja.
3. Análise de Sazonalidade
- Foi realizada uma consulta SQL para verificar padrões sazonais nas vendas do produto AWC Logo Cap na loja 1002.
- A análise revelou variações recorrentes em determinados meses, sugerindo comportamento sazonal.
4. Comparação de Crescimento por Região
- Os dados foram segmentados em dois grupos: Provincias (EUA) e Países (resto do mundo).
- Utilizou-se o modelo Prophet para prever a demanda futura de cada grupo.
- A previsão indicou maior crescimento no grupo Países, com base na demanda estimada para os próximos 3 meses.
5. Estimativa de Insumos (Zíperes para Luvas)
- Foi realizada uma previsão específica para produtos do tipo Gloves.
- A demanda prevista foi convertida em número de zíperes necessários, considerando dois zíperes por par de luvas.
- Resultado: 2.245 zíperes estimados para os próximos três meses.

📁 Estrutura dos Dados
- produto: nome do item vendido
- id_loja: identificador da loja
- ano_mes: data agregada mensalmente
- qtde: quantidade vendida
- rf, xgb, lgb: previsões dos modelos
- ma: previsão por média móvel
- rf_mae, rf_rmse, rf_r2: métricas de avaliação para Random Forest (idem para os outros modelos)

📈 Visualizações
- Gráficos de séries temporais foram gerados para ilustrar tendências, sazonalidade e previsões.
- As visualizações incluem intervalos de confiança e projeções futuras, facilitando a interpretação dos resultados.

✅ Conclusão
A abordagem adotada permitiu gerar previsões detalhadas e confiáveis, mesmo em cenários com dados limitados. A combinação entre modelos supervisionados e técnicas estatísticas simples, como média móvel, garantiu flexibilidade e robustez. As análises regionais e de insumos agregaram valor estratégico ao projeto, oferecendo insights práticos para planejamento e tomada de decisão.
