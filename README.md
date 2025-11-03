# Research: Traumatic Experiences & Brain (Image Classification + Segmentation)

This repo skeleton mirrors the plan outlined. Start with **classification** on a medical image dataset, then add **segmentation** later. It’s designed for **Kaggle (GPU)** training and **PyCharm** local scripting.

## Quickstart (Classification)
1. **Open Kaggle Notebook** → Enable **GPU** and **Internet**.
2. Add your dataset as an **Input** (e.g., `Add data` → search or upload). The expected layout for the starter notebook is:
   ```
   dataset_root/
     classA/
       img1.jpg
       ...
     classB/
       img2.jpg
       ...
   ```
3. In `configs/config.yaml`, set `dataset_root` to the Kaggle input path (e.g., `/kaggle/input/my-dataset`).
4. Run `notebooks/01_classification_baseline.ipynb` top to bottom.
5. Outputs saved to `reports/` (ROC, confusion matrix, metrics JSON).

## Repo Layout
```
research-trauma-brain/
├─ notebooks/
│  └─ 01_classification_baseline.ipynb
├─ src/
│  ├─ data/      # loaders & transforms
│  ├─ train/     # train helpers
│  ├─ eval/      # metrics & plots
│  └─ viz/       # visualization utils
├─ configs/
│  └─ config.yaml
├─ reports/      # figures, tables, metrics
└─ README.md
```

## Notes
- Keep **subject-wise splits** for medical data to avoid leakage.
- Use the segmentation template later to extract ROI features (mean Dice as the main metric).
- Document dataset provenance and ethics in your final report.
