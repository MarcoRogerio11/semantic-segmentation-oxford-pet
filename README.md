# Segmentação Semântica com U-Net utilizando o Dataset Oxford-IIIT Pet

## Disciplina

Processamento de Imagens

## Programa

Mestrado em Informática

## Objetivo

Desenvolver, treinar e avaliar um modelo de segmentação semântica baseado na arquitetura U-Net para identificação de regiões de interesse em imagens do dataset Oxford-IIIT Pet. O projeto foi implementado utilizando PyTorch e executado no Google Colab.

## Dataset

O conjunto de dados utilizado foi o Oxford-IIIT Pet Dataset, amplamente empregado em tarefas de visão computacional e segmentação semântica.

Características do dataset:

* Imagens de cães e gatos de diferentes raças
* Máscaras de segmentação anotadas
* Segmentação em nível de pixel
* Disponível através da biblioteca Torchvision

## Arquitetura Utilizada

O modelo desenvolvido foi baseado na arquitetura U-Net, uma das arquiteturas mais utilizadas para tarefas de segmentação semântica.

Principais características:

* Encoder para extração de características
* Decoder para reconstrução espacial
* Conexões de salto (skip connections)
* Saída pixel a pixel para classificação da imagem

## Pré-processamento

As seguintes etapas foram aplicadas:

* Redimensionamento das imagens para 128 × 128 pixels
* Conversão para tensores
* Normalização dos dados
* Divisão em conjuntos de treino, validação e teste

Distribuição do dataset:

* Treino: 2576 imagens
* Validação: 552 imagens
* Teste: 552 imagens

## Treinamento

Configurações utilizadas:

* Framework: PyTorch
* Otimizador: Adam
* Função de perda: CrossEntropyLoss
* Número de épocas: 10
* Execução em GPU (CUDA)

## Avaliação

O desempenho do modelo foi avaliado utilizando métricas tradicionais de segmentação semântica.

### Resultados Obtidos

| Métrica                       | Valor |
| ----------------------------- | ----- |
| Accuracy                      | 71.9% |
| IoU (Intersection over Union) | 64.9% |

## Resultados Visuais

O repositório contém:

* Curva de treinamento
* Imagem original
* Máscara real
* Máscara predita pelo modelo

Esses resultados permitem avaliar visualmente a qualidade da segmentação produzida pela rede neural.

## Estrutura do Repositório

```text
segmentacao-semantica-oxford-pet/
│
├── Segmentação_Pet_UNet.ipynb
├── unet_pet_segmentation.pth
├── curva_treinamento.png
├── predicao_segmentacao.png
└── README.md

## Tecnologias Utilizadas

* Python
* PyTorch
* Torchvision
* NumPy
* Matplotlib
* Google Colab

## Arquivos Disponíveis

### Segmentação_Pet_UNet.ipynb

Notebook contendo todo o pipeline de treinamento, validação, avaliação e visualização dos resultados.

### unet_pet_segmentation.pth

Pesos treinados do modelo U-Net.

### curva_treinamento.png

Curva de evolução da função de perda durante o treinamento.

### predicao_segmentacao.png

Exemplo de segmentação contendo:

* Imagem original
* Máscara real
* Máscara predita

## Considerações Finais

Os resultados obtidos demonstram a capacidade da arquitetura U-Net em realizar segmentação semântica de imagens do dataset Oxford-IIIT Pet. O modelo alcançou resultados satisfatórios tanto quantitativamente, através das métricas Accuracy e IoU, quanto qualitativamente, por meio das máscaras geradas.

## Autor

Marco Rogério

Mestrado em Informática

Disciplina: Processamento de Imagens

Universidade Federal de Alagoas (UFAL)
