# 📈 Previsão de Movimentos do S&P 500 com Machine Learning

Este é um projeto simples e introdutório que utiliza técnicas básicas de Machine Learning para prever se o índice **S&P 500** irá subir no próximo dia de negociação.

> Projeto desenvolvido como forma de estudo e curiosidade sobre a aplicação de ML no mercado financeiro.

## 🔧 Tecnologias Utilizadas

- Python
- [VS Code + extensão Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
- [yfinance](https://pypi.org/project/yfinance/)
- pandas
- scikit-learn
- matplotlib (opcional)

## 📌 O que o projeto faz

- Coleta dados históricos do S&P 500 (`^GSPC`) com o `yfinance`
- Remove colunas irrelevantes (dividendos e splits)
- Cria uma coluna `Target` que representa se o preço fechará **acima** do fechamento anterior
- Treina um modelo de **Random Forest Classifier** com variáveis básicas (preço de fechamento, abertura, volume, etc.)
- Realiza **backtest** com separação temporal (janela deslizante)
- Gera novas variáveis com médias móveis e tendências de diferentes períodos
- Ajusta o threshold de decisão com `predict_proba` para melhorar a precisão

## 📁 Estrutura do Código

O código está organizado em células para ser executado com facilidade no **Jupyter Notebook dentro do VS Code**. As principais etapas incluem:

1. **Coleta e limpeza de dados**
2. **Criação das variáveis alvo e preditoras**
3. **Treinamento e teste do modelo**
4. **Backtest e avaliação dos resultados**
5. **Expansão das features com médias móveis e tendência**

## 📊 Resultados

- Métrica principal: `precision_score`
- O modelo realiza previsões binárias (subida ou queda no próximo dia)
- A estratégia de avaliação respeita a ordem temporal dos dados (sem "data leakage")

## 📚 Possíveis Evoluções

- Inclusão de indicadores técnicos (RSI, MACD, etc.)
- Teste com modelos mais avançados (XGBoost, LSTM)
- Implementação de walk-forward validation
- Integração com APIs para sinais em tempo real

## ⚠️ Aviso

> Este projeto **não é uma recomendação de investimento**. É apenas um experimento educacional com fins de aprendizado sobre análise de dados e Machine Learning.

## 📎 Link do post no LinkedIn

Você pode ver uma explicação mais visual do projeto https://www.linkedin.com/posts/vitorribeirorosa_github-vitorrosa0stockmarketpredict-ml-activity-7330638026563338240-JAQj?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEdIrrIBKkQF0bytRV9y4nc7Hp0u_pnwvuc
