## Deep Learning Team Project – DiminuNet

This project aimed to develop an AI model that classifies leaf images based on whether the leaves show signs of disease.

By experimenting with architectures such as **ResNet** and **VGG16**, we explored **DiminuNet: an approach to achieving strong performance with a smaller model**.

### Model Selection Rationale (Why VGGNet?)

We experimented with both VGGNet and ResNet not simply to compare predictive accuracy, but to examine **performance relative to model complexity**.

ResNet uses skip connections to facilitate the training of deep networks, often achieving strong performance. However, deeper or larger variants can require substantial computational resources.

VGGNet, by contrast, has a straightforward, sequential architecture that is easy to understand and modify. Although standard VGG models are not necessarily lighter than ResNet in terms of parameters or computation, their simple structure provided a useful starting point for exploring architectural modifications.

Our central research question was:

> **Can a simplified or modified VGG-based architecture achieve performance comparable to ResNet while reducing model complexity?**

Through this investigation, we sought to explore:

- How network depth and architectural complexity affect performance
- The potential and limitations of lightweight models
- Criteria for model selection based on the **performance–efficiency trade-off**

### Challenges with the Original Dataset

- The dataset contained approximately **400 leaf images**, which was relatively small for training a deep learning model.
- Although the task was binary classification, the dataset was **class-imbalanced**, with substantially more healthy-leaf images than diseased-leaf images.

### Techniques Explored

#### 01. SMOTE

We experimented with **Synthetic Minority Over-sampling Technique (SMOTE)** to address class imbalance.

Although SMOTE is typically applied to tabular feature data, we explored applying it to images by **flattening them into feature vectors**.

#### 02. Data Augmentation

We applied random image transformations, including **cropping, rotation, and blurring**, to increase the diversity of the training data.

#### 03. Batch Normalization and Dropout

To improve generalization, we experimented with adding **batch normalization** and **dropout** to different layers and compared multiple architectural configurations.
