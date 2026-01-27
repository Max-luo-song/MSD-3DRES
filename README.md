<div align="center">

# 🎯 Multi-Source Disambiguation for 3D Referring Expression Segmentation


</div>

## 🔍 Introduction

**Multi-Source Disambiguation for 3D Referring Expression Segmentation (MSD-3DRES)** is a groundbreaking framework that tackles one of the most challenging problems in 3D vision-language understanding: **3D Referring Expression Segmentation (3D-RES)**. Unlike existing methods that struggle with real-world ambiguities, our approach specifically addresses multi-source uncertainties through innovative ambiguity-tolerant learning mechanisms.

<div style="text-align: center;">
    <img src="assets/introductionv3.png" alt="Method Overview" width="100%">
</div>

### 🎯 What Problem Do We Solve?

Real-world 3D referring expressions often suffer from three types of ambiguity:
- **Prompt Ambiguity**: Vague or underspecified language descriptions
- **Spatial Ambiguity**: Viewpoint-dependent spatial relationships  
- **Annotation Ambiguity**: Inconsistent or noisy training labels

3D-ATRES provides the first comprehensive solution to simultaneously handle all these challenges.

## ✨ Key Innovations

<div align="center">

| Feature | Innovation | Impact |
|---------|------------|--------|
| **🔄 TR² Semantic Structurizer** | Transforms free-form language into structured Target–Relation–Referent triples | Eliminates **prompt ambiguity** through semantic disambiguation |
| **🧭 Normal-Aware Spatial Alignment** | Incorporates surface normal cues for geometric reasoning | Ensures **viewpoint-invariant** spatial understanding |
| **📊 Annotation Ambiguity Penalty** | Probabilistic learning with ambiguity-aware loss functions | Robust to **inconsistent annotations** during training |

</div>

## 🏆 Performance Highlights

### State-of-the-Art Results on Major Benchmarks

<div align="center">

| Method | Venue | Base LLM | ScanRefer Acc@0.25 | ScanRefer Acc@0.5 | Multi3DRefer F1@0.25 | Multi3DRefer F1@0.5 |
|--------|-------|----------|-------------------|------------------|---------------------|--------------------|
| **Specialist Models** | | | | | | |
| ScanRefer (Chen et al., 2020) | ECCV'20 | – | 42.4 | 26.0 | – | – |
| BUTD-DETR (Jain et al., 2022) | ECCV'22 | – | 50.4 | 38.6 | – | – |
| M3DRef-CLIP (Zhang et al., 2023) | ICCV'23 | – | – | 44.7 | 42.8 | 38.4 |
| 3D-VisTa (Zhu et al., 2023) | ICCV'23 | – | 50.6 | 45.8 | – | – |
| EDA (Wu et al., 2023) | CVPR'23 | – | 54.6 | 42.2 | – | – |
| D-LISA (Zhang et al., 2024) | NeurIPS'24 | – | 57.0 | 46.2 | – | – |
| MCLN (Guo et al., 2025) | ECCV'24 | – | 57.1 | 45.5 | – | – |
| G³-LQ (Wang et al., 2024) | CVPR'24 | – | 56.9 | 45.6 | – | – |
| GPS (Jia et al., 2024) | CVPR'24 | – | – | 48.1 | – | – |
| 3D-VLP (Yang et al., 2024) | AAAI'24 | – | 51.7 | 40.5 | – | – |
| ConcreteNet (Unal et al., 2024) | ECCV'24 | – | 56.1 | 49.5 | – | – |
| **LLM-based Models** | | | | | | |
| 3D-LLM (Hong et al., 2023) | NeurIPS'23 | BLIP2-flant5 | 30.3 | – | – | – |
| PQ3D (Zhu et al., 2024c) | ECCV'24 | Vicuna-7B | 57.0 | 51.2 | – | – |
| ReGround3D (Zhu et al., 2024a) | ECCV'24 | BLIP2-flant5 | 53.1 | 41.1 | – | – |
| Chat-Scene (Huang et al., 2024) | NeurIPS'24 | Vicuna-7B | 55.5 | 50.2 | 57.1 | 52.4 |
| LIBA (Wang et al., 2024c) | AAAI'25 | – | 59.6 | 49.0 | – | 50.2 |
| Inst3D-LMM (Yu et al., 2025) | CVPR'25 | Vicuna1.5-7B | 57.8 | 51.6 | 58.3 | 53.5 |
| Video-3D LLM (Zheng et al., 2025) | CVPR'25 | LLaVA-Video 7B | 58.1 | 51.7 | 58.0 | 52.7 |
| 3D-LLaVA (Zhu et al., 2024b) | CVPR'25 | LLaVA-1.5-7B | 62.8 | 45.3 | 68.7 | 49.2 |
| MSD-3DRES* (Ours) | – | LLaVA-1.5-7B | 65.3 | 50.3 | 72.7 | 55.5 |
| MSD-3DRES (Ours) | – | LLaVA-1.5-7B | 65.9 | 50.5 | 73.7 | 55.8 |

</div>

> 💡 **Key Insight**: Our method achieves particularly significant gains in challenging scenarios with complex spatial relationships and ambiguous descriptions, demonstrating superior ambiguity tolerance.

## 🌐 Live Demo

### Experience 3D-ATRES in Action

We provide an **[interactive online demo](http://521661fbe9494e65b3805ad5028c5cc1.cloud.lanyun.net:10000/)** where you can:

- 📤 Upload your own point clouds
- 💬 Test with custom referring expressions  
- 👁️ View real-time segmentation results
- 📊 Compare with baseline methods

### Demo Examples

#### Example 1: Complex Spatial Relationships
<div align="center">
    <img src="assets/example1.gif" alt="Example 1" width="600">
</div>

#### Example 2: Ambiguous Object Descriptions  
<div align="center">
    <img src="assets/example2.gif" alt="Example 2" width="600">
</div>

#### Example 3: Multi-Object Scenarios
<div align="center">
    <img src="assets/example3.gif" alt="Example 3" width="600">
</div>

## 🗓️ Release Timeline

- [x] **Jan. 2026**: Visualization tools released (`web2.4_EN/`)
- [ ] **Paper Accepted**: Training code and pretrained models
- [ ] **Paper Accepted**: Full documentation and tutorials
- [ ] **Paper Accepted**: Extended benchmarks and applications

## 🤝 Contributing

We welcome contributions from the community! Areas of interest include:

- 🎯 New benchmark evaluations
- 🔧 Performance optimizations  
- 📚 Additional documentation and tutorials
- 🌍 Multi-language support

*Contributing guidelines will be released with the code.*

