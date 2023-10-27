# RMT
Official code for "RMT: Retentive Networks Meet Vision Transformer"

[Arxiv](https://arxiv.org/abs/2309.11523)

## Abstract

Retentive Network first emerged in the domain of NLP and immediately gained widespread attention due to its remarkable performance. A significant portion of its impressive capabilities stems from its explicit decay mechanism, which incorporates valuable prior knowledge. However, this explicit decay is unidirectional and one-dimensional, making it unsuitable for the bidirectional, two-dimensional modeling required in image-based tasks. To solve this, we propose a bidirectional, two-dimensional form of explicit decay specifically designed for vision models to introduce distance-related prior knowledge. Besides, unlike language models, the vision backbones use the same parallel form during training and inference. If this parallel form is replaced with recurrent or chunk-wise recurrent form, the parallelism of the model will be significantly disrupted, resulting in extremely slow inference speed. So we discard the two additional inference modes present in the original RetNet, retaining only the parallel form. Specifically, we incorporate bidirectional, two-dimensional explicit decay into the Self-Attention to form **Re**tentive **S**elf-**A**ttention (ReSA). Furthermore, to reduce the complexity of global modeling, we decompose ReSA along the two axes of the image. Building upon ReSA, we construct RMT, a strong vision backbone. Abundant experiments have demonstrated that our RMT exhibits exceptional performance across various computer vision tasks. For example, RMT achieves **84.1** Top1-acc on ImageNet-1k using merely **4.5G** FLOPs. To the best of our knowledge, among all models, RMT achieves the highest Top1-acc when models are of similar size and trained with the same strategy. Moreover, RMT significantly outperforms existing vision backbones in downstream tasks.![RMT](RMT.png)

## Citation

If you use RMT in your research, please consider the following BibTeX entry and giving us a star:
```BibTeX
@misc{fan2023rmt,
      title={RMT: Retentive Networks Meet Vision Transformers}, 
      author={Qihang Fan and Huaibo Huang and Mingrui Chen and Hongmin Liu and Ran He},
      year={2023},
      eprint={2309.11523},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```
