# 🍷 Wine Quality Classification — POSTECH Fase 2

Classificação da qualidade de vinhos com Machine Learning usando o [Wine Quality Dataset](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset).

## Objetivo

Prever se um vinho é de **alta qualidade** (nota ≥ 7) ou **baixa/média qualidade** (nota < 7) com base em suas características físico-químicas.

## Estrutura do Projeto

```
wine-quality-classification/
│
├── data/
│   └── WineQT.csv              # Dataset original
├── notebooks/
│   └── wine_quality_classification.ipynb  # Análise completa
├── src/                        # Scripts auxiliares (opcional)
├── results/                    # Gráficos e métricas gerados
│   ├── 01_balanceamento_classes.png
│   ├── 02_distribuicao_features.png
│   ├── 03_correlacao.png
│   ├── 04_boxplots.png
│   ├── 05_comparacao_modelos.png
│   ├── 06_curvas_roc.png
│   ├── 07_matrizes_confusao.png
│   ├── 08_feature_importance.png
│   ├── 09_feature_importance_comparacao.png
│   └── metricas_modelos.csv
├── requirements.txt
└── README.md
```

## Como Executar

```bash
# 1. Clone o repositório
git clone <url-do-repo>
cd wine-quality-classification

# 2. Instale as dependências
pip install -r requirements.txt

# 3. Abra o notebook
jupyter notebook notebooks/wine_quality_classification.ipynb
```

## Pipeline de Análise

1. **Compreensão do Problema** — definição da variável alvo binária
2. **EDA** — distribuições, correlações, outliers, balanceamento
3. **Pré-processamento** — normalização + feature engineering
4. **Modelos** — Regressão Logística, Random Forest, Gradient Boosting
5. **Avaliação** — Acurácia, F1, ROC-AUC, Matrizes de Confusão
6. **Interpretação** — importância das features e recomendações

## Principais Resultados

| Modelo | ROC-AUC | F1-Score |
|--------|---------|----------|
| Regressão Logística | ~0.79 | ~0.60 |
| Random Forest | ~0.87 | ~0.70 |
| **Gradient Boosting** | **~0.88** | **~0.71** |

> Os valores exatos são gerados ao executar o notebook.

## Features Mais Importantes

1. `alcohol` — teor alcoólico
2. `volatile acidity` — acidez volátil
3. `sulphates` — sulfatos
4. `citric acid` — ácido cítrico
5. `density` — densidade

## Dataset

- **Fonte:** [Kaggle — Wine Quality Dataset](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)
- **Amostras:** 1.143 vinhos tintos
- **Features:** 11 características físico-químicas
- **Target:** qualidade (transformada em binária)
