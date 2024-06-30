# Visual Question Answering in Medical Imaging (VQA-Med)
## Introduction
Visual Question Answering (VQA) systems represent a field of research in deep learning that combines natural language processing (NLP) and computer vision to answer questions about images. The primary goal of such systems is to detect features present in the images and questions presented to the model and produce answers based on the captured characteristics.

In the medical context, Visual Question Answering Medical (VQA-Med) stands out by applying these techniques to interpret medical images and answer fundamental questions for diagnostics and treatments. The complexity arises not only from the diversity of questions, which range from binary to contextual, but also from the need to effectively integrate visual and textual information for precise responses. This integration is crucial to avoid excessive simplifications of complex questions or unnecessary complications of simple questions, aspects that often challenge current VQA-Med systems [Bazi et al. 2023].

The relevance of this task does not make it less complex. The generality of the questions that can be asked by the end-user of the application is one example of this complexity. Questions can have binary answers (yes or no) or can be more complex, requiring detailed and context-dependent responses. VQA-Med techniques sometimes fail to differentiate these types of questions, resulting in unnecessary complexity for simple problems or an oversimplification of more complex problems. To address this variability, it is crucial to implement attention mechanisms that allow for the simultaneous understanding of both the visual content of images and the textual content of questions. These mechanisms ensure appropriate contextualization of the question in relation to the image, increasing the accuracy and relevance of the provided answers.

In this project, we present a VQA-Med application using data from ImageClef2019, with images exclusively from the medical domain. For the development of the application, we utilized the pre-trained convolutional neural network ResNet-50 for the computer vision task and the pre-trained BERT model for the question-answering task. We used multi-head attention mechanisms for feature retrieval throughout the network and attribute fusion via concatenation at the end of the two networks. The features were concatenated and then passed through multi-head attention and subsequently through a fully connected (FC) layer. Additionally, we evaluated the impact of fine-tuning on the image network.

The structure of this work is as follows: first, a theoretical framework on VQA models developed specifically for medical data and in general is presented in Section 2.
Next, in Section 3, we present the flowchart of the model architecture, the origin of the data used, the pre-trained models, and their adjustments (fine-tuning). Finally, in Section 4, we present the model results, including the choice of hyperparameters, loss metrics, and result visualization.

## Networks
You can find the models in the *models* folder

## Data and pre-trained models
Data and the pre-trained models can be found in google drive: https://drive.google.com/drive/folders/1Sfy5Rafvk53Numl8TzYUCrhVq3WvzuJL?usp=sharing

