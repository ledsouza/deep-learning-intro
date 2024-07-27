## Classificação de Roupas com Deep Learning 👚👖

![Static Badge](https://img.shields.io/badge/Status-Finalizado-green)

## Descrição

Este projeto implementa um modelo de Deep Learning para classificar imagens de roupas do dataset Fashion MNIST. O modelo utiliza uma rede neural com camadas densas (fully connected) e dropout para evitar overfitting.

## Tecnologias Utilizadas

- Python
- TensorFlow
- Keras
- Plotly

## Descrição Detalhada do Projeto

### Dataset Fashion MNIST

O dataset Fashion MNIST consiste em 70.000 imagens em escala de cinza de 28x28 pixels, divididas em 10 categorias de roupas:

- Camiseta
- Calça
- Pullover
- Vestido
- Casaco
- Sandália
- Camisa
- Tênis
- Bolsa
- Bota

O dataset é dividido em 60.000 imagens para treino e 10.000 para teste.

### Arquitetura do Modelo

O modelo implementado é uma rede neural sequencial com as seguintes camadas:

1. **Flatten:** Converte as imagens 28x28 em um vetor unidimensional de 784 elementos.
2. **Dense (256 unidades, ativação ReLU):** Camada densa com 256 neurônios e função de ativação ReLU.
3. **Dropout (0.2):** Camada de dropout com taxa de 0.2 para evitar overfitting.
4. **Dense (10 unidades, ativação Softmax):** Camada de saída com 10 neurônios (um para cada categoria) e função de ativação Softmax para gerar probabilidades para cada classe.

### Treinamento

O modelo é treinado utilizando o otimizador Adam e a função de perda SparseCategoricalCrossentropy. O treinamento é realizado por 5 épocas com uma divisão de validação de 20%.

### Avaliação

A performance do modelo é avaliada utilizando as métricas de acurácia e perda, tanto para o conjunto de treino quanto para o de validação. Os resultados são visualizados em gráficos gerados com a biblioteca Plotly.

### Salvamento e Carregamento

O modelo treinado é salvo em um arquivo 'modelo.keras' utilizando a função `model.save()`. Posteriormente, o modelo é carregado a partir do arquivo utilizando a função `keras.models.load_model()`.

### Previsões

O modelo carregado é utilizado para fazer previsões em novas imagens do conjunto de teste. As previsões são comparadas com as labels reais para verificar a acurácia do modelo.

## Observações

Este projeto foi desenvolvido como parte de um curso da Alura e serve como introdução aos conceitos básicos de Deep Learning com TensorFlow e Keras. O modelo implementado é relativamente simples e pode ser aprimorado com a utilização de arquiteturas mais complexas, como redes neurais convolucionais (CNNs).
