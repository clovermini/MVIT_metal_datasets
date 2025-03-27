# MVIA_metal_datasets
*Provided by Machine Vision and Industrial Application Laborator (MVIA Lab).*

## 📌 Overview
We release two metal surface defect datasets with instance-level pixel annotations: Casting Billet, Steel Pipe.

## 🗃️ Datasets
### 1. Casting Billet Dataset
- **Images**: 1,060 (780 defective)
- **Resolution**: 96×106 to 3,228×492
- **Defect Types**:
  - Scratch
  - Weld slag 
  - Cutting opening
  - Water slag mark
  - Slag skin
  - Longitudinal crack

### 2. Steel Pipe Dataset
- **Images**: 1,227 (554 defective) 
- **Resolution**: 728×544 (fixed)
- **Defect Types**:
  - Warp
  - External fold
  - Wrinkle 
  - Scratch

## ✏️ Annotation Process
1. **AI Pre-segmentation**: Input Bounding Box Annotations and Images: Utilize SAM's predictor interface to perform batch automatic segmentation, generating initial masks.

2. **Expert Refinement**:
     1): Identify suboptimal segmentation results from the initial masks through human review.
     2): Interactive Refinement: For poorly segmented data, apply SAM's interactive segmentation by iteratively adding. Positive sample points to guide target region identification. Negative sample points to exclude interference regions. Update segmentation results in real-time until achieving desired accuracy.
    3). Post-processing:
      (1)Perform threshold-based segmentation with optimal thresholds for suitable data;
      (2)Apply morphological operations: Open operation and closed operation are used for edge smoothing, noise elimination, hole filling and other operations.

![Label Process](samples/label_process.png)

## 🖼️ Samples
![Dataset Samples](samples/datasets.png)

## 📥 Download
[Download Link](#) | [Alternative Mirror](#)

## 📜 Citation

## 📧 Contact
For dataset inquiries or collaboration opportunities:  📧 [xuke@ustb.edu.cn](mailto:xuke@ustb.edu.cn) 📧 [chuniliu@xs.ustb.edu.cn](mailto:chuniliu@xs.ustb.edu.cn)

---

**Maintained by** [MVIA Lab](https://cicst.ustb.edu.cn/rcpy/yjsds/bssds1/2d415f8ca1f54cc6abafe9b7c10ba665.htm) @ [Collaborative Innovation Center of Steel Technology](https://cicst.ustb.edu.cn/), [University of Science and Technology Beijing](https://www.ustb.edu.cn)
