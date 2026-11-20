<div align="center">📊 Avaliação de Modelos de Inteligência Artificial
Um projeto de aprendizado sobre métricas, previsões e comparação de modelos

Explorando como avaliar resultados preditivos e interpretar o desempenho de diferentes modelos.
</div>🎯 Sobre o projeto
Este projeto foi desenvolvido para praticar a avaliação e comparação de modelos preditivos, utilizando métricas estatísticas e visualizações para entender como diferentes previsões se comportam em relação aos valores reais.

O exercício compara quatro conjuntos de previsões — PRED, PRED_2, PRED_3 e PRED_4 — com os valores observados (TRUE), analisando a qualidade dos resultados e possíveis sinais de underfitting, overfitting e viés sistemático (bias).
💡 Proposta: um projeto de aprendizado, com foco em compreender métricas e desenvolver pensamento analítico — não em construir um modelo pronto para produção.

🧰 Tecnologias e ferramentas
Ferramenta	Utilização
Python	Linguagem utilizada no projeto
Pandas e NumPy	Manipulação e análise dos dados
Matplotlib e Seaborn	Visualização dos resultados
Scikit-learn	Métricas de avaliação
Jupyter Notebook	Desenvolvimento e documentação das análises


📐 Metodologia de avaliação
A comparação foi realizada por meio de visualizações e três métricas principais:
Métrica	O que avalia	Como interpretar
R²	Quanto da variação dos valores reais é explicada pelas previsões.	Quanto mais próximo de 1, melhor o ajuste. Pode ser negativo.
MAPE	Erro percentual absoluto médio.	Quanto menor, menor o erro percentual médio.
Bias	Erro médio com sinal (previsão - valor real).	Próximo de zero indica pouco erro sistemático médio. Positivo indica tendência a superestimar; negativo, a subestimar.


Além das métricas, foram utilizados:
- Gráficos de linhas: comparação entre valores previstos e observados.
- Gráficos de dispersão: análise da proximidade das previsões em relação à linha ideal (y = x).
📊 Resultados
Métricas calculadas a partir de 1.094 observações da planilha:
Modelo	R²	MAPE	Bias
PRED	0.9326	4.0887%	-0.0024
PRED_2	0.99997	0.0919%	-0.0002
PRED_3	0.1111	15.6829%	-0.0476
PRED_4	-3.1408	39.5481%	-3.0024


🔎 Análise dos modelos
<details>
<summary><strong>Modelo PRED</strong> — bom desempenho geral</summary>Apresenta bom ajuste, R² elevado, erro percentual relativamente baixo e Bias médio muito próximo de zero. É um resultado consistente, embora não seja o melhor nas métricas desta comparação.
</details><details>
<summary><strong>Modelo PRED_2</strong> — melhores métricas da comparação</summary>
Apresenta os melhores resultados numéricos: R² praticamente igual a 1, MAPE muito baixo e Bias próximo de zero.

O notebook levanta a hipótese de overfitting para esse modelo. Entretanto, métricas calculadas sobre uma única série de previsões não comprovam overfitting; é necessário comparar resultados em dados de treino e validação/teste.
</details><details>
<summary><strong>Modelo PRED_3</strong> — possível underfitting</summary>
Apresenta baixo R² e MAPE mais elevado, indicando dificuldade em acompanhar os valores observados. O comportamento é compatível com um possível underfitting, conforme a interpretação visual do exercício.

O Bias médio é relativamente pequeno, mostrando que um erro médio próximo de zero não significa, por si só, boas previsões.
</details><details>
<summary><strong>Modelo PRED_4</strong> — forte tendência de subestimação</summary>
Apresenta R² negativo, MAPE elevado e Bias de aproximadamente -3.00. Isso indica previsões muito distantes dos valores reais e uma forte tendência a subestimar os resultados.
</details>🧠 Conclusões e aprendizados
A principal lição deste exercício foi entender que não basta observar um gráfico ou utilizar apenas uma métrica para escolher um modelo. É importante combinar indicadores quantitativos e análise visual para compreender diferentes aspectos dos erros.

Com os dados disponíveis:
- PRED_2 obteve o melhor desempenho quantitativo.
- PRED também demonstrou boa capacidade preditiva.
- PRED_3 apresentou sinais de ajuste insuficiente.
- PRED_4 revelou um forte viés de subestimação.
Outro aprendizado importante é que um modelo com métricas excelentes não é automaticamente um modelo confiável. É necessário avaliar sua capacidade de generalização em dados que não foram utilizados no treinamento.
Não existe um modelo universalmente perfeito: a escolha depende dos dados, do problema e do comportamento esperado em situações reais.

🚀 Próximos passos
- [ ] Separar os dados em conjuntos de treino, validação e teste.
- [ ] Comparar o desempenho dentro e fora do conjunto de treinamento.
- [ ] Investigar a possível ocorrência de overfitting no PRED_2.
- [ ] Explorar outras métricas, como MAE e RMSE.
- [ ] Avaliar a distribuição dos resíduos e possíveis padrões nos erros.
<div align="center">Projeto desenvolvido para fins educacionais

Consolidando conhecimentos sobre avaliação de modelos preditivos, métricas de regressão e interpretação de resultados em Ciência de Dados.
</div>
