#ShopMais Retention Analytics

## Engenharia de Features, EDA e Machine Learning para previsão de churn em e-commerce

Este projeto simula um case real de analytics para uma empresa fictícia de e-commerce chamada **ShopMais**.

O objetivo foi identificar fatores associados ao churn de clientes e desenvolver um modelo preditivo capaz de priorizar clientes com maior risco de abandono.

---

# Objetivos do projeto

- analisar churn de clientes;
- tratar dados reais com valores ausentes;
- criar features orientadas a negócio;
- gerar insights acionáveis;
- construir segmentação de risco;
- desenvolver modelo preditivo de churn;
- estimar impacto financeiro do churn.

---

# Dataset

Base pública de churn em e-commerce contendo informações de:

- comportamento de compra;
- tempo de relacionamento;
- satisfação;
- reclamações;
- uso do aplicativo;
- pedidos;
- cashback;
- recência de compra.

---

# Principais etapas

## 1. Auditoria e limpeza dos dados

- tratamento de valores ausentes;
- criação de flags de ausência;
- padronização de colunas;
- análise de qualidade dos dados.

## 2. Engenharia de features

Features criadas:

- tenure_group;
- recency_group;
- satisfaction_group;
- complaint_satisfaction_risk;
- engagement_score;
- coupon_intensity;
- cashback_per_order;
- warehouse_distance_group.

## 3. EDA focada em negócio

Principais perguntas respondidas:

- clientes novos cancelam mais?
- reclamações aumentam churn?
- satisfação explica retenção?
- clientes inativos possuem maior risco?
- quais segmentos devem ser priorizados?

## 4. Machine Learning

Modelo utilizado:

- Random Forest Classifier

Principais métricas:

- ROC AUC: 0.92
- Recall (churn): 82.7%
- Accuracy: 86.1%

---

# Principais insights

## Clientes novos concentram maior risco

Clientes com até 3 meses apresentaram churn de 41,9%, muito acima da média da base.

## Reclamações são forte sinal de churn

Clientes com reclamação tiveram churn de 31,67%, quase 3 vezes maior do que clientes sem reclamação.

## Satisfação isolada não explica retenção

A análise mostrou que satisfação precisa ser interpretada em conjunto com reclamações e comportamento de compra.

## O modelo consegue separar clientes de alto risco

Clientes classificados como alto risco apresentaram churn real de 63,5%.

---

# Resultados visuais

## Churn por tempo de relacionamento

![Churn por Tenure](images/churn_tenure.png)

## Curva ROC

![ROC Curve](images/roc_curve.png)

## Variáveis mais importantes

![Feature Importance](images/feature_importance.png)

---

# Tecnologias utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Google Colab
- Jupyter Notebook

---

# Estrutura do projeto

```text
shopmais-churn-eda/
```

---

# Conclusão

O projeto mostrou que o churn da ShopMais está fortemente associado à fase inicial do relacionamento com o cliente.

Os resultados indicam que estratégias de onboarding, retenção inicial e acompanhamento de reclamações possuem alto potencial de impacto.

Além disso, o modelo preditivo demonstrou capacidade prática de priorizar clientes por risco de churn, permitindo integração futura com CRM e campanhas preventivas.
