## Papers in Deep Clustering

- [ Shen, Yuming, et al. "You Never Cluster Alone." *Conference and Workshop on Neural Information Processing Systems (NIPS)*. 2021. ](https://arxiv.org/pdf/2106.01908.pdf)
-  [Niu, Chuang, Hongming Shan, and Ge Wang. "Spice: Semantic pseudo-labeling for image clustering." *IEEE Transactions on Pattern Analysis and Machine Intelligence (TPAMI).* 2021.](https://arxiv.org/pdf/2103.09382.pdf) 

- [Tsai, Tsung Wei, Chongxuan Li, and Jun Zhu. "MiCE: Mixture of Contrastive Experts for Unsupervised Image Clustering." *International Conference on Learning Representations (ICLR)*. 2021.](https://openreview.net/pdf?id=gV3wdEOGy_V)
  - **MiCE** (Mixture of Contrastive Experts) can be seen as the discriminative model for instance discrimination with latent variable, where the EM algorithm is used to solve then nontrivial inference problem. The whole training procedure is basically same with that of MoE. As for the loss function, MiCE introduce the dot product between the instances and the cluster prototypes for the experts, encouraging a clear cluster structure around the prototype. However, the training epochs are too  large to be accepted, for example, it takes 6000 epochs to train STL-10 and 3000 epochs to train ImageNet-Dog. Also, it might be challenging when training datasets with excessive clusters (e.g., Tiny-ImageNet with 200 clusters).
- [ Do, Kien, Truyen Tran, and Svetha Venkatesh. "Clustering by Maximizing Mutual Information Across Views." *Proceedings of the IEEE international conference on computer vision (ICCV). * 2021. ](https://arxiv.org/pdf/2107.11635.pdf)
  - **CRLC**
- [Zhang, Dejiao, et al. "Supporting Clustering with Contrastive Learning." *Annual Conference of the North American Chapter of the Association for Computational Linguistics (NAACL).* 2021.](https://arxiv.org/pdf/2103.12953.pdf)
  - Applied in text data. **SCCL** = DEC + Contrastive Learning.
- [ Zhao, Han, et al. "Graph Debiased Contrastive Learning with Joint Representation Clustering.“ *IJCAI*. 2021.  ](https://www.ijcai.org/proceedings/2021/0473.pdf)
  - = DEC in graph data  + Contrastive Learning
- [Li, Yunfan, et al. "Contrastive clustering." *2021 AAAI Conference on Artificial Intelligence (AAAI)*. 2021.](https://www.aaai.org/AAAI21Papers/AAAI-1352.LiY.pdf)
  - **CC** = Contrastive Learning (instance-level contrastive head) + PICA (cluster-level contrastive head). it takes 1000epochs to train each dataset.
- [Bo, Deyu, et al. "Structural deep clustering network." *Proceedings of The Web Conference 2020 (WWW)*. 2020.](https://dl.acm.org/doi/pdf/10.1145/3366423.3380214?casa_token=htTAxhfH6xkAAAAA:k_Smn2T5LsruzuW4gbdgqEP-BEXBBAbLSCnBwK2ciTKiOSY2sYqiHgHkq2yjCjengkHkS8DF3wuv)
  - **SDCN** = DEC with the GNN structure.
- [Huang, Jiabo, Shaogang Gong, and Xiatian Zhu. "Deep semantic clustering by partition confidence maximisation." *Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)*. 2020.](https://openaccess.thecvf.com/content_CVPR_2020/papers/Huang_Deep_Semantic_Clustering_by_Partition_Confidence_Maximisation_CVPR_2020_paper.pdf)
  - **PICA**: PUI(Partition Uncertainty Index) is in fact equal to the cluster-level contrastive head in **CC**.
- [Ji, Xu, Joao F. Henriques, and Andrea Vedaldi. "Invariant information clustering for unsupervised image classification and segmentation." *Proceedings of the IEEE/CVF International Conference on Computer Vision (ICCV)*. 2019.](https://openaccess.thecvf.com/content_ICCV_2019/papers/Ji_Invariant_Information_Clustering_for_Unsupervised_Image_Classification_and_Segmentation_ICCV_2019_paper.pdf)
  - Opposed to merely maximizing entropy , **IIC** turns to maximize mutual information  between encoded variables of paired data samples. The advantage is that the maximizing mutual information contains maximizing individual cluster assignments entropy H(z) and thus avoids the degenerate solution
- [Chang, Jianlong, et al. "Deep adaptive image clustering." *Proceedings of the IEEE international conference on computer vision (ICCV)*. 2017.](https://openaccess.thecvf.com/content_ICCV_2017/papers/Chang_Deep_Adaptive_Image_ICCV_2017_paper.pdf)
  - **DAC**
- [ Hu, Weihua, et al. "Learning discrete representations via information maximizing self-augmented training." *International conference on machine learning (ICML) *. PMLR, 2017. ](http://proceedings.mlr.press/v70/hu17b/hu17b.pdf)
  - **IMSAT**
- [Yang, Bo, et al. "Towards k-means-friendly spaces: Simultaneous deep learning and clustering." *international conference on machine learning (ICML)*. PMLR, 2017.](http://proceedings.mlr.press/v70/yang17b/yang17b.pdf)
  - **DCN**
- [Xie, Junyuan, Ross Girshick, and Ali Farhadi. "Unsupervised deep embedding for clustering analysis." *International conference on machine learning (ICML)*. PMLR, 2016.](http://proceedings.mlr.press/v48/xieb16.pdf)
  - Given the DNN parameters and the initial centroids, **DEC** first measure the similarity (i.e., probability distribution ) Q between embedded points and centroid with the help of student's t distribution. Then it introduces the auxiliary target distribution P by raising q to the second power and normalize by frequency per cluster.  The model is trained by minimizing the KL divergence between P and Q. it is significant that the auxiliary target distribution P should strengthen predictions, put more emphasis on data points assigned with high confidence, and be normalized.
