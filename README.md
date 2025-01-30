# Liver Tumor Detection using YOLOv8: Size-Adaptive Nanoparticle Design Based on Tumor Dimensions

## Overview
This repository implements a liver tumor detection system leveraging YOLOv8 for precise tumor localization in MRI images. The system utilizes the tumor's dimensions to recommend an optimal nanoparticle size for treatment, bridging the gap between diagnostic accuracy and personalized therapy design. The method combines the power of AI with nanotechnology for enhancing liver cancer diagnosis and treatment.

# Liver Tumor Detection using YOLOv8: Size-Adaptive Nanoparticle Design Based on Tumor Dimensions

## Overview
This repository implements a liver tumor detection system leveraging YOLOv8 for precise tumor localization in MRI images. The system uses tumor dimensions to recommend an optimal nanoparticle size for treatment, bridging the gap between diagnostic accuracy and personalized therapy design. The method combines AI and nanotechnology for enhanced liver cancer diagnosis and treatment.

## Methodology

### **Figure: Methodology for Liver Tumor Detection with YOLOv8 and Adaptive Nanoparticle Sizing Based on Tumor Dimensions**

![Methodology Diagram](https://github.com/Rehab-Alsaidi/LNV/blob/main/assets/methodology_diagram.png)

This methodology outlines the pipeline for liver tumor detection and characterization, combining deep learning with feature-based analysis for optimal nanoparticle design.

1. **YOLOv8 Object Detection**:
   - **YOLOv8** is used to localize liver tumors in MRI images. This model is known for its speed and accuracy, detecting the presence and location of tumors and marking them with bounding boxes.

2. **Crop the Tumor Region**:
   - After detecting the tumor, we crop the tumor region from the MRI image for focused analysis, reducing irrelevant data and improving model performance.

3. **Segment Tumor Shape**:
   - A binary mask is created by applying thresholding techniques to the tumor region, allowing clear delineation between the tumor and surrounding tissue. This step isolates the tumor's boundaries for further analysis.

4. **Extract Tumor Features**:
   - Several features are extracted from the segmented tumor region, including:
     - **Bounding Box Dimensions**: Position and size of the bounding box around the tumor.
     - **Aspect Ratio**: Ratio of width to height of the tumor.
     - **Perimeter**: Total boundary length of the tumor.
     - **Area**: Number of pixels within the tumor region.
     - **Major and Minor Axes**: The longest and shortest diameters of the tumor, respectively.
   - These features are key to understanding the tumor's geometry and are used for nanoparticle design.

5. **Connect Tumor Features to Nanoparticle Design**:
   - Tumor features, such as diameter and aspect ratio, are used to determine the optimal nanoparticle size for targeted drug delivery. A set of rules is applied, derived from studies on drug release from vasculature-bound nanoparticles.

### **Tumor Diameter and Corresponding Nanoparticle Design Parameters**

| Tumor Diameter at Start of Treatment (µm) | Tumor Diameter (TD) (nm) | Nanoparticle Size (TNP) (nm) |
|-----------------------------------------|-------------------------|------------------------------|
| 105                                     | 1000                    | 125                          |
| 188                                     | 777                     | 729                          |
| 366                                     | 520                     | 535                          |
| 425                                     | 678                     | 447                          |
| 517                                     | 352                     | 404                          |
| 675                                     | 382                     | 322                          |
| 760                                     | 334                     | 288                          |
| 813                                     | 276                     | 285                          |

These values demonstrate how tumor size (TD) influences the selection of the nanoparticle size (TNP), which plays a critical role in optimizing drug delivery.

6. **Optimize Nanoparticle Parameters**:
   - The final step involves optimizing the nanoparticle parameters for effective drug delivery. By using the extracted tumor features, nanoparticles are tailored for better interaction with the tumor and to maximize therapeutic efficacy.

## Results
- **Detection**: YOLOv8 demonstrated high accuracy in liver tumor localization, achieving a precision of 94%, recall of 96%, and mAP@0.5 of 59%.
- **Nanoparticle Design**: The methodology correlates tumor dimensions with nanoparticle sizes, ensuring effective targeted therapy. Tumor size directly impacts nanoparticle design, enhancing treatment efficiency.

### Performance Metrics
- **Precision**: 94%
- **Recall**: 96%
- **mAP@0.5**: 59%

## Conclusion
This study showcases how AI and nanotechnology can be integrated for improved liver cancer diagnosis and treatment. The YOLOv8-based detection system provides accurate tumor localization, and the nanoparticle design methodology offers a tailored approach to therapy. This framework serves as a step toward personalized medicine, combining computer vision with nanoparticle-based solutions for effective liver tumor management.

