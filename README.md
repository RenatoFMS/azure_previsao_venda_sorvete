# 🍦 Previsão de Vendas de Sorvete com Azure Machine Learning

Este projeto foi desenvolvido como parte dos meus estudos em **Inteligência Artificial** e **Machine Learning**, focando na aplicação prática de modelos preditivos em nuvem. O objetivo é prever a quantidade de sorvetes vendidos com base na temperatura externa utilizando a plataforma **Microsoft Azure**.

## 📊 O Dataset
O conjunto de dados simula o desempenho de uma loja de sorvetes e contém as seguintes variáveis:
* **Data**: Registro cronológico no formato AAAA-MM-DD.
* **Quantidade_Vendida**: Volume de vendas diárias (Variável Alvo/Target).
* **Temperatura**: Temperatura máxima do dia em graus Celsius (Variável Preditora).

> O dataset completo está em `vendas_sorvete.csv` .

## 🛠️ Ferramentas e Tecnologias
* **Azure Machine Learning Service**: Gerenciamento de experimentos e modelos.
* **Azure ML Designer**: Criação de pipelines de dados via interface visual.
* **Automated ML (AutoML)**: Processo automatizado que identificou o melhor algoritmo para o cenário.
* **Algoritmo Vencedor**: **XGBoostRegressor**.

## 🚀 Fluxo de Trabalho (Pipeline)
O modelo seguiu um fluxo estruturado no Azure ML Designer:


1. **Importação de Dados**: Carregamento do arquivo CSV higienizado.
2. **Seleção de Colunas**: Identificação dos atributos relevantes.
3. **Divisão de Dados (Split)**: Separação entre dados de treino e teste.
4. **Treinamento e Score**: Aplicação do modelo e geração de predições individuais.
5. **Avaliação**: Cálculo das métricas de erro para validar a confiabilidade.

## 📈 Resultados e Métricas
O modelo de **Automated ML** obteve resultados de alta precisão, com um erro normalizado (NRMSE) de apenas **0.050**. Abaixo, as métricas detalhadas obtidas no bloco Evaluate Model:

* **Mean Absolute Error (MAE)**: 4.58 (erro médio de ~5 sorvetes por previsão).
* **Root Mean Squared Error (RMSE)**: 6.09.
* **Relative Squared Error**: 0.047.

### Comparativo: Real vs. Predição (Scored Labels)
| Valor Real (Vendas) | Temperatura (°C) | Predição da IA |
| :--- | :--- | :--- |
| 190 | 38 | 189.52 |
| 135 | 31 | 128.49 |
| 105 | 28 | 102.33 |

---

### Imagens da execução:
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/985b5be9-29e9-47c9-8b7b-46206dd413ee" />
<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/3967260e-23a2-407c-bb4b-56eb74ad8a31" />

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/d431527e-35d4-4cee-abd4-fa8e1d2c5f7e" />

<img width="500" height="500" alt="image" src="https://github.com/user-attachments/assets/e01e87cf-907f-491f-b66d-a6f2852b6bf8" />


