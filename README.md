# Knowledge Distillation for Skin Lesion Classification


<div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/knowledge-distillation/blob/master/Knowledge_Distillation_for_Skin_Lesion_Classification.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
</div>


The goal of knowledge distillation is to improve the performance of the half-witted model, which, most of the time, has fewer parameters, by allowing it to learn from the more competent model or the teacher model. The half-witted model, or the student model, excerpts the knowledge from the teacher model by matching its class distribution to the teacher model's. To make the distributions softer (used in the training process as part of the loss function), we can adjust a temperature _T_ to them (this is done by dividing the logits before softmax by the temperature). This project designates EfficientNet-B0 as the teacher and SqueezeNet v1.1 as the student. These models will be experimented on the DermaMNIST dataset of MedMNIST. We will take a look at the performance of the teacher, the student (without knowledge distillation), and the student (with knowledge distillation) in the result section.


## Experiment


To witness the distillation in action, please refer to the notebook at the following [link](https://github.com/reshalfahsi/knowledge-distillation/blob/master/Knowledge_Distillation_for_Skin_Lesion_Classification.ipynb).



## Result

## Quantitative Result

The quantitative results are delivered below in the form of a table.

Model | Loss | Accuracy |
------------ | ------------- | ------------- |
Teacher |  2.271 | 71.99% |
Student | 2.025 | 70.77% |
Distilled | 7.409 | 71.17% |


## Validation Accuracy and Loss Curve

### Teacher

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/teacher_loss_curve.png" alt="teacher_loss_curve" > <br /> The loss curve on the train set and the validation set of the teacher model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/teacher_acc_curve.png" alt="teacher_acc_curve" > <br /> The accuracy curve on the train set and the validation set of the teacher model. </p>

### Student

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/student_loss_curve.png" alt="student_loss_curve" > <br /> The loss curve on the train set and the validation set of the student model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/student_acc_curve.png" alt="student_acc_curve" > <br /> The accuracy curve on the train set and the validation set of the student model. </p>


### Distilled

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/distilled_loss_curve.png" alt="distilled_loss_curve" > <br /> The loss curve on the train set and the validation set of the distilled model. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/distilled_acc_curve.png" alt="distilled_acc_curve" > <br /> The accuracy curve on the train set and the validation set of the distilled model. </p>


### Overall

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/overall_acc.png" alt="overall_acc" > <br /> Comparison of loss curves between the teacher model, the student model, and the distilled model on the validation set. </p>

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/overall_loss.png" alt="overall_loss" > <br /> Comparison of loss curves between the teacher model, the student model, and the distilled model on the validation set. </p>


## Qualitative Result

The qualitative results of the models on the test set are exhibited in the collated form below.


### Teacher

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/teacher_qualitative.png" alt="teacher_qualitative" > <br /> The qualitative result of the teacher model. </p>


### Student

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/student_qualitative.png" alt="student_qualitative" > <br /> The qualitative result of the student model. </p>


### Distilled

<p align="center"> <img src="https://github.com/reshalfahsi/knowledge-distillation/blob/master/assets/distilled_qualitative.png" alt="distilled_qualitative" > <br /> The qualitative result of the distilled model. </p>


## Credit

- [Knowledge Distillation](https://keras.io/examples/vision/knowledge_distillation/)
- [Distilling the Knowledge in a Neural Network](https://arxiv.org/pdf/1503.02531.pdf)
- [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/abs/1905.11946)
- [SqueezeNet v1.1](https://github.com/forresti/SqueezeNet/tree/master/SqueezeNet_v1.1)
- [MedMNIST v2 - A large-scale lightweight benchmark for 2D and 3D biomedical image classification](https://medmnist.com/)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
