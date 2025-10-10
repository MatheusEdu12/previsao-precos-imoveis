# Previsão de Preços de Imóveis

Projeto baseado no livro *Mãos à Obra: Aprendizado de Máquina*. Utiliza o dataset California Housing e tem como objetivo analisar dados de imóveis e construir modelos de machine learning para prever preços de casas com base em características demográficas e geográficas.

## Estrutura do Projeto

- **data/**  
  - **raw/**: Dados brutos  
  - **processed/**: Dados processados para modelagem  
- **images/**: Imagens e visualizações  
- **models/**: Modelos treinados  
- **notebooks/**: Notebooks de exploração, preprocessamento, modelagem e avaliação  
- Dockerfile  
- docker-compose.yml  
- requirements.txt  

## Notebooks

- **01_exploracao.ipynb**: Exploração inicial do dataset, análise estatística, visualização geográfica e criação de novas features.  
- **02_preprocessamento.ipynb**: Preprocessamento dos dados, pipelines de transformação e escalonamento, separação entre variáveis preditoras e alvo.  
- **03_modelagem.ipynb**: Treinamento de modelos de regressão (Linear, Decision Tree, Random Forest), ajuste de hiperparâmetros e validação cruzada.  
- **04_avaliacao.ipynb**: Avaliação da performance dos modelos usando RMSE no conjunto de teste e comparação entre os modelos.

## Tecnologias

- Python  
- Bibliotecas: pandas, numpy, scikit-learn, matplotlib, joblib  
- Docker (para execução em container)

## Como Executar com Docker

1. Certifique-se de ter Docker e Docker Compose instalados.  
2. No diretório do projeto, construa e execute a imagem Docker:
```docker-compose --build up -d```

4. Acesse o Jupyter Notebook no navegador (URL indicada no terminal) e execute os notebooks na ordem:
   - 01_exploracao.ipynb  
   - 02_preprocessamento.ipynb  
   - 03_modelagem.ipynb  
   - 04_avaliacao.ipynb  

## Resultados

O projeto gera modelos de regressão capazes de prever preços médios de imóveis, com avaliação de performance via RMSE para cada modelo:

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  

Os modelos treinados são salvos na pasta `models` e podem ser reutilizados para novas previsões.

