# 🎓 Classificação Multiclasse: Previsão do Desfecho Acadêmico de Estudantes

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/VictorGMSS/Classifica-o_multiclasse/blob/main/classificacao_multiclasse.ipynb)

Projeto prático desenvolvido durante o curso na **"Alura"**. O objetivo deste repositório é prever o desfecho acadêmico de estudantes (**Desistente**, **Graduado** ou **Matriculado**), aplicando análise exploratória, pré-processamento, modelagem com **Random Forest**, balanceamento de classes com **SMOTE** e validação correta por meio de um **pipeline** com validação cruzada.

---

## 🎯 Objetivos do Projeto

* **Análise Exploratória de Dados (EDA):** Investigar dados demográficos, socioeconômicos, de matrícula e acadêmicos para identificar padrões associados a cada desfecho.
* **Pré-processamento:** Transformar variáveis categóricas com **One-Hot Encoding** e separar os dados em treino, validação e teste de forma estratificada.
* **Modelagem Multiclasse:** Treinar um classificador **Random Forest** e controlar o sobreajuste ajustando a profundidade das árvores.
* **Avaliação do Desempenho:** Analisar a **matriz de confusão** (absoluta e normalizada) e o relatório de métricas por classe (precisão, recall e F1-score).
* **Balanceamento de Dados:** Aplicar a técnica de superamostragem **SMOTE** para melhorar o desempenho nas classes minoritárias.
* **Validação Correta:** Usar um **pipeline** (`imblearn`) com **StratifiedKFold**, evitando vazamento de dados ao balancear apenas os dados de treino de cada fold.
* **Interpretação dos Resultados:** Comparar os resultados antes e depois do balanceamento e testar o modelo final em dados nunca vistos.

---

## 🗂️ Estrutura do Repositório

* `classificacao_multiclasse.ipynb`: Notebook principal com todo o pipeline de exploração, pré-processamento, modelagem, balanceamento e validação.
* `dados_estudantes.csv`: Base de dados de estudantes, com variáveis demográficas, socioeconômicas, macroeconômicas, de matrícula e de desempenho acadêmico, e a variável alvo `Target` (`Desistente`, `Graduado` e `Matriculado`).

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

* **Python 3**
* **Pandas:** Manipulação dos dados e montagem do conjunto final codificado.
* **Matplotlib, Seaborn & Plotly:** Visualizações exploratórias (distribuições, `countplot`, boxplots e gráficos de barras interativos).
* **Scikit-Learn:** `OneHotEncoder`, `train_test_split`, `RandomForestClassifier`, `confusion_matrix`, `ConfusionMatrixDisplay`, `classification_report`, `cross_validate` e `StratifiedKFold`.
* **Imbalanced-Learn:** `SMOTE` para superamostragem e `Pipeline` (`imbpipeline`) para validar o balanceamento corretamente.

---

## 🚀 Etapas Desenvolvidas no Notebook

1. **Conhecendo os Dados:** Carregamento da base (`[PREENCHER]` registros), inspeção com `info()` e identificação das classes da variável alvo.
2. **Exploração dos Dados:** Análise de dados demográficos (estado civil, idade na matrícula, sexo e estrangeiros), socioeconômicos (devedor, taxas em dia e bolsista), de matrícula (curso) e acadêmicos (notas do 1º e 2º semestres), sempre relacionados ao `Target`, além da análise da proporção de cada classe.
3. **Pré-processamento:** Aplicação de **One-Hot Encoding** em 11 variáveis categóricas e separação dos dados em treino, validação e teste (`15%` para teste, com estratificação).
4. **Treinamento:** Ajuste do **Random Forest** padrão e com `max_depth=10`, comparando a acurácia de treino e de validação para identificar sobreajuste.
5. **Avaliação:** Análise da matriz de confusão e do relatório de classificação por classe.
6. **Balanceamento com SMOTE:** Superamostragem das classes minoritárias no treino e reavaliação das métricas e da matriz de confusão normalizada.
7. **Validação com Pipeline:** Validação cruzada estratificada (`5` folds) com **SMOTE + Random Forest** no mesmo pipeline, usando o **recall ponderado** (`recall_weighted`) e calculando um intervalo de confiança aproximado (média ± 2 desvios-padrão). Resultado: `[PREENCHER]`.
8. **Teste Final:** Treino do modelo com os dados balanceados e avaliação em dados de teste nunca vistos (recall ponderado no teste: `[PREENCHER]`).

---

## 💻 Como Executar

1. **Via Google Colab (Recomendado):** Clique no botão **"Open in Colab"** no topo deste README para abrir e executar o notebook diretamente no navegador sem precisar configurar ambiente local.
2. **Localmente:**
```bash
git clone https://github.com/VictorGMSS/Classifica-o_multiclasse.git
cd Classifica-o_multiclasse
pip install pandas matplotlib seaborn plotly scikit-learn imbalanced-learn jupyter
jupyter notebook classificacao_multiclasse.ipynb
```

---

## 👨‍💻 Informações pessoais

Victor Gabriel Martins e Souza

* 💼 LinkedIn: [https://www.linkedin.com/in/victorgms](https://www.linkedin.com/in/victorgms)
* 🌐 Portfólio: [https://verxstech.vercel.app](https://verxstech.vercel.app)
