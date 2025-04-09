
# Siamese Network com ResNet50 para Verificação de Similaridade Facial

Este projeto implementa uma **Siamese Network** baseada na arquitetura **ResNet50** como extratora de características, com o objetivo de verificar a **semelhança entre rostos de celebridades**. As imagens são provenientes de um dataset pós-processado e organizadas por identidade.

## 🧠 O que é Metric Learning?

**Metric Learning** é uma abordagem de aprendizado de máquina cujo objetivo é aprender uma função de similaridade entre pares de exemplos. Em vez de classificar imagens diretamente, aprende-se uma **métrica de distância** no espaço latente, onde imagens semelhantes estão próximas e diferentes estão distantes.

Neste projeto, o Metric Learning é implementado por meio de uma **Siamese Network**, que compara vetores de características extraídos de duas imagens para determinar se pertencem à mesma identidade.

## 🧩 Arquitetura da Rede

- **Backbone**: [ResNet50](https://keras.io/api/applications/resnet/#resnet50-function), sem as camadas de classificação finais.
- **Siamese Network**: consiste em duas redes idênticas que compartilham pesos, aplicadas separadamente a cada imagem de um par.
- **Camada de distância**: calcula a distância Euclidiana entre os embeddings das imagens.
- **Função de perda**: *Contrastive Loss*, que penaliza pares semelhantes distantes e pares diferentes próximos.
- **Métrica principal**: Acurácia binária para verificação de similaridade.


## ⚙️ Dependências

- Python 3.x
- TensorFlow / Keras
- NumPy
- OpenCV
- Matplotlib
- Google Colab (opcional)


## 📈 Resultados

O modelo aprende gradualmente a discriminar rostos semelhantes e diferentes, alcançando uma **acurácia satisfatória após cerca de 50 épocas**. Essa abordagem é útil em sistemas de verificação de identidade, reconhecimento de faces e autenticação.

