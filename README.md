# Image-Driven Analysis of Bubble Dynamics and Foam Stability
<img width="1389" height="789" alt="image" src="https://github.com/user-attachments/assets/a8e323e0-a010-40b2-b8d1-0ac787b7e595" />


**Microscopy Hackathon 2025 – AISCIA Informatics**
---

## Author : **Hesham Eina Abdalla**  
*Electrical Engineer | Embedded Systems | AI & Microscopy*  
Qatar University Alumni

- **GitHub:** https://github.com/hdaw1905  
- **LinkedIn:** https://www.linkedin.com/in/hesham-eina/

---

This repository contains the final submission notebook for an **image-driven, explainable machine learning analysis of foam stability**, using time-resolved microscopy images to link **bubble-scale dynamics** to **macroscopic foam behavior**.

---

## 🚀 Open in Google Colab (Recommended)

👉 https://colab.research.google.com/drive/1fhaQA016Q5WfzfI3khMvToaWtjyYj8P3?usp=sharing

---

## 📌 How to Run (Judges)

1. Download the dataset from:  
   https://drive.google.com/drive/folders/1O1y_lesCDsoj3T3hb9_en9Q1v9cR2eQ-?usp=sharing

2. Unzip the dataset and upload the folder  
   `AI_Microscopy_FoamDynamics`  
   to your Google Drive (**My Drive**).

3. Open the notebook using the Google Colab link above.

4. Run the notebook **from top to bottom**.

No code modification is required.

---

## 🧰 Libraries Used

- **NumPy** – numerical computing  
- **Pandas** – data handling and time-series analysis  
- **Matplotlib** – scientific visualization  
- **SciPy** – statistical analysis  
- **scikit-image** – image segmentation, morphology, and region analysis  
- **scikit-learn** – explainable regression modeling  
- **tqdm** – progress tracking  

*Note: Google Colab already includes most of these libraries by default.*

If running outside Google Colab, install dependencies using:

```bash
pip install numpy pandas matplotlib scipy scikit-image scikit-learn tqdm
```

## 🔁 End-to-End Image-Driven Workflow

Microscopy Images  
→ Binary Segmentation of Bubbles 
<img width="1189" height="348" alt="image" src="https://github.com/user-attachments/assets/a228f6d7-e344-44d4-a154-02aa20a1053f" />

→ Bubble Geometry & Spatial Feature Extraction  
<img width="431" height="354" alt="image" src="https://github.com/user-attachments/assets/536becfc-2f12-4a5e-a883-0d08844856e2" />

→ Temporal Dynamics (Coarsening, Entropy, Packing)  
<img width="781" height="470" alt="image" src="https://github.com/user-attachments/assets/d6272f00-4fca-4eb0-b2aa-5750da5695c8" />

→ Image-Derived Foam Stability Proxies  
→ Explainable Machine Learning  
<img width="730" height="393" alt="image" src="https://github.com/user-attachments/assets/5e6ca3c1-491a-4b2d-bf9e-45049539de83" />

→ Physical Interpretation  

All results are derived directly from microscopy images, without relying on chemical parameters or empirical fitting.

--- 

## 🧪 Findings — Image-Driven Bubble Dynamics and Foam Stability

This study demonstrates that foam stability can be explained and compared using **only microscopy images**, by quantifying how bubble populations evolve over time under different nanoparticle conditions.

---

### 🔹 Bubble Coarsening Dynamics
<img width="859" height="470" alt="image" src="https://github.com/user-attachments/assets/f6dbc0c4-f914-4b01-8f4e-74064dba5fd6" />

Analysis of the **mean bubble area over time** reveals distinct coarsening behaviors across the three experiments:

- **Baseline foam (E138 – surfactant only)** exhibits rapid early coarsening, with bubble sizes increasing quickly and stabilizing at relatively small values.
- **GO-stabilized foam (E130 – 150 ppm GO)** shows a markedly slower coarsening rate, with a more gradual increase in mean bubble area across frames.
- **NGO-stabilized foam (E142 – 1500 ppm NGO)** displays intermediate behavior, with slower early coarsening than the baseline but stronger late-stage growth than GO.

These trends are consistently visible both in the **coarsening curves** and directly in the **microscopy images**.

---

### 🔹 Bubble Persistence and Population Decay
<img width="790" height="470" alt="image" src="https://github.com/user-attachments/assets/09d2fd81-5a13-4162-acd0-4e4b8a5924ad" />

Bubble count dynamics provide a direct measure of foam collapse and persistence:

- The **baseline foam** experiences the fastest bubble loss, indicating rapid film rupture and foam degradation.
- **GO-stabilized foam** maintains the highest bubble count across nearly all frames, demonstrating strong resistance to collapse.
- **NGO-stabilized foam** retains bubbles longer than the baseline but shows more pronounced late-stage bubble loss than GO.

---

### 🔹 Bubble Size Distribution and Heterogeneity
<img width="1289" height="397" alt="image" src="https://github.com/user-attachments/assets/e9f7b5b2-ae2e-4063-b03f-d824fba9ddfc" />

Size-distribution analysis extracted directly from segmented microscopy images shows clear differences in bubble heterogeneity:

- **Baseline foam** rapidly loses small bubbles, leading to a narrow and low-entropy size distribution.
- **GO-stabilized foam** maintains a broader size distribution for longer times, reflected by higher and more sustained entropy values.
- **NGO-stabilized foam** exhibits intermediate entropy levels, indicating controlled but not maximal size uniformity.

Log-scale histograms and percentile trends confirm that **GO suppresses the formation of very large bubbles**, slowing Ostwald ripening.

---

### 🧠 Image-Derived Foam Stability Ranking
<img width="590" height="390" alt="image" src="https://github.com/user-attachments/assets/92b57424-8613-49e8-b970-a9e0a5e9fdc8" />

A foam stability proxy was computed from **bubble persistence and population dynamics**:

| Experiment | Condition                         | Foam Stability Proxy |
|-----------:|-----------------------------------|---------------------:|
| **E130**   | Surfactant + 150 ppm GO            | **20991.9** |
| **E142**   | Surfactant + 1500 ppm NGO          | 2478.4 |
| **E138**   | Surfactant only (baseline)         | 1406.2 |

**GO-stabilized foam** is therefore the most stable, followed by **NGO**, with the **baseline foam** being the least stable.

---

### 🤖 Explainable Machine Learning Insights

An explainable regression model reveals that **early-time microscopic features** carry predictive information about foam stability:

- **Early coarsening rate** is the strongest positive contributor.
- **Early entropy change** and **spatial packing dynamics** negatively impact stability.
- **Bubble loss rate** contributes at a smaller but measurable level.

These results indicate that **foam stability can be inferred from early-stage bubble dynamics**, before macroscopic collapse occurs.

---

## 🏁 Conclusion — Linking Microscopy to Foam Stability

This work demonstrates that **microscopy images alone contain sufficient information** to explain and compare foam stability across different nanoparticle formulations.

By extracting interpretable **bubble-level and spatial features** from segmented images and modeling their temporal evolution, we link **graphene oxide particle size directly to foam behavior**. Large graphene oxide particles slow bubble coarsening, preserve size heterogeneity, and sustain bubble populations more effectively than nano-sized particles or surfactant-only formulations.

Importantly, the entire analysis is **image-driven and chemistry-agnostic**, relying only on visual patterns and time ordering. This highlights the potential of **explainable machine learning** to bridge microscopy observations and macroscopic material performance.

More broadly, this workflow is reusable for other **cellular and porous systems**, enabling early prediction of stability and failure from microscopic dynamics alone.

## 📚 Reference

Benali, B., & Foyen, T. (2022). *Pore-scale Bubble Population Dynamics of CO₂-Foam at Reservoir Pressure, Dataset and Segmented Images*. **Mendeley Data**, Version 1. https://doi.org/10.17632/5d37nbzf9s.1  
Dataset link: https://data.mendeley.com/datasets/5d37nbzf9s/1


