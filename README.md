# Modelo de Predição de Clientes para Investimento

Este repositório contém a implementação de um modelo de classificação para predição do comportamento de clientes ao realizar investimentos. O projeto utiliza engenharia de atributos com variáveis dummy e algoritmos de machine learning, incluindo árvore de decisão, para classificar se um cliente aderirá ou não a investimentos.

## Descrição

O modelo foi desenvolvido para analisar dados de marketing de investimento e prever a aderência dos clientes a produtos de investimento. Utiliza-se análise exploratória de dados, pré-processamento com one-hot encoding e label encoding, e comparação de modelos de classificação.

## Funcionalidades

- Análise exploratória de dados categóricos e numéricos
- Pré-processamento de dados com one-hot encoding e normalização
- Treinamento e comparação de modelos: Dummy Classifier, Árvore de Decisão e KNN
- Visualização da árvore de decisão
- Exportação e carregamento de modelos treinados usando Pickle
- Predição para novos dados

## Especificações Técnicas

### Linguagem e Ambiente
- **Linguagem**: Python 3.x
- **Ambiente**: Jupyter Notebook

### Bibliotecas Principais
- `pandas`: Manipulação e análise de dados
- `plotly.express`: Visualização de dados interativa
- `scikit-learn`: Algoritmos de machine learning (preprocessing, model_selection, tree, dummy, neighbors)
- `matplotlib.pyplot`: Plotagem de gráficos (para visualização da árvore)
- `pickle`: Serialização de objetos Python (para salvar/carregar modelos)

### Algoritmos Utilizados
- **Dummy Classifier**: Modelo baseline baseado na frequência da classe alvo
- **Árvore de Decisão**: Modelo principal, com ajuste de profundidade máxima
- **K-Nearest Neighbors (KNN)**: Modelo de comparação, com normalização de dados

### Dados
- **Fonte**: Arquivo CSV `marketing_investimento.csv` localizado na pasta `data/`
- **Variáveis**:
  - `idade`: Idade do cliente (numérica)
  - `estado_civil`: Estado civil (categórica: casado(a), divorciado(a), solteiro(a))
  - `escolaridade`: Nível de escolaridade (categórica: fundamental, médio, superior)
  - `inadimplencia`: Se o cliente tem inadimplência (categórica: sim/não)
  - `saldo`: Saldo bancário (numérica)
  - `fez_emprestimo`: Se fez empréstimo (categórica: sim/não)
  - `tempo_ult_contato`: Tempo desde o último contato (numérica)
  - `numero_contatos`: Número de contatos realizados (numérica)
  - `aderencia_investimento`: Variável alvo (categórica: sim/não)

## Como Executar

### Pré-requisitos
1. **Python 3.x**: Certifique-se de ter o Python instalado (recomendado 3.8 ou superior).
2. **Jupyter Notebook**: Instale via pip ou conda.
   ```bash
   pip install jupyter
   ```
3. **Bibliotecas**: Instale as dependências listadas.
   ```bash
   pip install pandas plotly scikit-learn matplotlib
   ```

### Passos para Execução
1. **Clone ou baixe o repositório** para o seu ambiente local.
2. **Navegue até a pasta do projeto**:
   ```bash
   cd modelo-predicao-clientes-investimento
   ```
3. **Abra o Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
4. **Execute o notebook** `modelo/modelo_previsao.ipynb`:
   - Abra o arquivo no navegador.
   - Execute as células sequencialmente (Shift + Enter).
   - As células incluem leitura de dados, análise exploratória, pré-processamento, treinamento de modelos e predições.

### Notas sobre Execução
- O notebook não foi executado ainda; execute todas as células para reproduzir os resultados.
- Os modelos treinados são salvos como arquivos `.pkl` (modelo_onehot.pkl e modelo_arvore.pkl).
- Para predições com novos dados, use o exemplo fornecido no final do notebook.

## Uso

Após executar o notebook, você pode:
- Visualizar gráficos de análise exploratória.
- Comparar acurácias dos modelos (Dummy, Árvore, KNN).
- Fazer predições para novos clientes fornecendo dados no formato esperado.
- Ajustar hiperparâmetros dos modelos (ex.: profundidade da árvore).

## Contribuição

Sinta-se à vontade para contribuir com melhorias, correções ou novas funcionalidades. Abra uma issue ou pull request no repositório.
