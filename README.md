# TrafficSigns-SafeRouteAI: Detecção de Sinais de Trânsito com IA

![Capa do Projeto](https://github.com/ViniciusKanh/TrafficSigns-SafeRouteAI/blob/main/assets/img/maxresdefault.jpg)

## 🚀 Introdução
O projeto _TrafficSigns-SafeRouteAI_ foi desenvolvido por Vinicius de Souza Santos, um apaixonado por tecnologia e inovação, com o objetivo de criar um sistema de reconhecimento de sinais de trânsito usando técnicas avançadas de Inteligência Artificial. O projeto utiliza uma abordagem prática e interativa para detectar e classificar sinais de trânsito alemães, contribuindo para sistemas de navegação mais seguros e eficientes.

## 📚 Metodologia

### Conjunto de Dados
O modelo foi treinado utilizando o _German Traffic Sign Recognition Benchmark (GTSRB)_, uma extensa base de dados contendo mais de 50.000 imagens de sinais de trânsito categorizadas em 43 classes.

### Tratamento de Dados
Antes de treinar o modelo, os dados passaram por um processo de normalização e ajuste. As imagens foram redimensionadas para 32x32 pixels, e o contraste foi ajustado para realçar detalhes importantes. Além disso, foi aplicada a técnica de _Data Augmentation_ para ampliar a variedade de dados, incluindo rotações e translações das imagens originais.

### Modelo de IA
O coração do projeto é um modelo de rede neural convolucional (_Convolutional Neural Network - CNN_) construído com TensorFlow e Keras. A rede foi projetada com camadas de convolução para extração de características, seguidas por camadas _Fully Connected_ para a classificação.

#### Arquitetura do Modelo:
1. Camadas Convolucionais com Batch Normalization e MaxPooling.
2. Camadas Densas com Dropout para reduzir overfitting.
3. Camada de saída com função de ativação Softmax para classificação multiclasse.

### Parâmetros do Modelo
- Taxa de aprendizado: 1e-3
- Épocas: 30
- Batch size: 64
- Otimizador: Adam
- Função de perda: Categorical Crossentropy

## 📈 Desempenho e Avaliação
O modelo demonstrou alta acurácia na classificação dos sinais de trânsito, com desempenho consistentemente melhorando ao longo das épocas de treinamento. A matriz de confusão e relatórios de classificação forneceram insights detalhados sobre o desempenho do modelo em diferentes classes.

## 🖥️ Código do Modelo

```python
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Conv2D, BatchNormalization, MaxPooling2D, Flatten, Dense, Dropout, Activation

# Inicializa o modelo
TrafficSignNet = Sequential()

# Adiciona as camadas do modelo
# ... (detalhes das camadas)

# Compila o modelo
TrafficSignNet.compile(
    loss="categorical_crossentropy",
    optimizer=Adam(lr=1e-3, decay=1e-3/30),
    metrics=["accuracy"]
)

# Treina o modelo
TrafficSignNet.fit( ... )
```

## 📋 Conclusão
Este projeto ilustra como a Inteligência Artificial pode ser efetivamente aplicada na detecção e classificação de sinais de trânsito, contribuindo para a segurança no trânsito e sistemas de navegação autônoma.

## 📞 Contato
- **Desenvolvedor**: Vinicius de Souza Santos
- **GitHub**: [ViniciusKanh](https://github.com/ViniciusKanh)
- **LinkedIn**: [Perfil no LinkedIn](https://www.linkedin.com/notifications/?filter=all)
- **E-mail**: [vinnyciussouza@outlook.com](mailto:vinnyciussouza@outlook.com)
