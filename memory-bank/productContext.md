# Product Context

## Why this project exists
Medical imaging reports often describe findings in natural language. "Grounding" these reports means mapping specific phrases in the report to specific regions in the image. This project focuses on the **PadChest-GR (Grounded Reports)** dataset, specifically its **Benchmark** subset.

## Problems it solves
- **Standardized Evaluation**: Uses the official "Benchmark" subset of PadChest (`study_is_benchmark=True`), allowing for fair comparison with other academic works.
- **Weakly Supervised Learning**: The dataset consists of automatically labeled data (`study_is_validation=False`), presenting a challenge for training robust models on noisy labels.
- **Multi-Label Classification**: Addresses the complexity of chest X-rays where a single image often contains multiple pathological findings.

## Dataset Characteristics
- **Size**: 4,555 unique images (filtered from the larger PadChest dataset).
- **Format**: Long-format CSV (multiple rows per image, one per label).
- **Quality**: 
    - **Labels**: Generated via NLP (not manually validated).
    - **Benchmark**: Yes, this is the designated test set for comparisons.
- **Content**: Contains both "Normal" cases and various pathologies, along with bounding box annotations.

## User Experience Goals
- Efficient data loading that aggregates multiple rows into single image-level samples.
- Clear visualization of data distributions (completed in `analysis.ipynb`).
- Reproducible research using the benchmark split.
