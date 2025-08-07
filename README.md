# deeplearn_MobileNetV2
Projeto de rede neural convolucional profunda (CNN) usando MobileNetV2


Projeto de rede neural convolucional profunda (CNN)

✅ Resumo Técnico do Projeto 🎯 Objetivo: Classificar imagens entre gatos e cachorros utilizando uma arquitetura de rede profunda pré-treinada (MobileNetV2) e refinar essa rede com Fine-Tuning para adaptar aos dados específicos.

🧠 Rede Profunda (Deep Network) Sim, estamos usando MobileNetV2, que é uma rede neural convolucional profunda (CNN) com dezenas de camadas (mais de 150), originalmente treinada no dataset ImageNet (com mais de 1 milhão de imagens e 1.000 classes).

🔁 Transfer Learning Transfer Learning = Reaproveitar o conhecimento aprendido em um grande dataset (ImageNet) para resolver um problema semelhante com um dataset menor (gatos e cachorros).

Como usamos no projeto: Importamos o modelo MobileNetV2 pré-treinado

Removemos a "cabeça" original da rede (camada de saída com 1.000 classes)

Adicionamos nossas próprias camadas finais (para 1 classe binária: gato ou cachorro)

Treinamos essas novas camadas com nossos dados

🔧 Tecnologias e Conceitos aplicados:

Conceito Aplicado? Como foi usado?

Deep Learning ✅ Uso de rede CNN profunda (MobileNetV2)

Transfer Learning ✅ Reutilização de pesos do ImageNet

CNN (Convolutional) ✅ Arquitetura com convoluções, pooling e flatten

Normalização de Imagem ✅ Imagens redimensionadas e normalizadas entre 0–1

Data Pipeline com TFDS ✅ Uso de tensorflow_datasets para carregar e dividir o dataset

Batching e Prefetching ✅ Uso de batch() e prefetch() para performance

🔎 Criado upload de fotos para avaliação:

Etapa Descrição

📤 files.upload() Abre um botão de upload no Colab

📸 Carrega imagem Converte a imagem para o tamanho e formato esperado

🔍 Predição Usa seu modelo model.predict()

🎯 Resultado Mostra se é gato (0.00) ou cachorro (1.00) com a imagem e confiança
