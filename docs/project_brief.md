# Project Brief

## User and Situation

### Who needs the system?
School nurses, community health workers, and dental screening personnel who conduct oral health check-ups for students and local residents on a regular basis.

### What happens now, and what should become better?
Currently, oral health screening is done entirely by human visual inspection — a screener looks at each tooth in photos and manually decides whether it looks healthy or has decay. This process is:
- Time-consuming when dealing with hundreds of students
- Prone to human error (fatigue, subjective judgment)
- Inefficient for large-scale screening programs

The system should assist screeners by automatically flagging teeth that show possible decay symptoms, so staff can focus their attention where it's needed most and reduce missed cases.

## What the System Should Do

### Input
Close-up oral and tooth photographs taken under conventional (non-specialist) lighting conditions, as would be captured by a standard camera or smartphone during school screening visits.

### Useful Output
A clear identification result for each tooth in the image, indicating whether it shows signs of:
- Healthy (no visible decay)
- Possible early-stage decay (discoloration, small pits)
- Obvious decay (visible cavities, significant erosion)

### Action or Decision After the Output
Screening staff review the system's flagged results and prioritize suspected problematic teeth for further manual examination and professional dental follow-up. The system does NOT replace professional diagnosis — it is an auxiliary screening aid only.

## Why AI May Help

### What pattern may need to be learned?
Tooth decay presents as diverse, irregular visual patterns — color spots (white/brown/black), surface texture changes (pits, erosion), and structural damage. These patterns vary significantly across individuals, making simple rule-based (if/then) approaches ineffective.

### What rules, interface, people, or review steps belong to the system?
- The AI model learns visual patterns from labeled image samples (healthy vs. decayed teeth)
- A simple interface presents results to screeners with clear visual markers (e.g., highlighted regions on teeth)
- Human professional review is required for ALL system identification results to avoid misdiagnosis
- The system outputs a screening priority list, not a medical diagnosis

## Initial Data Plan

### Where the data may come from
- Public open-source dental image datasets with health and decay labels (e.g., NIH dental datasets, Kaggle dental image collections)
- A small number of authorized real-scene oral photos for supplementary validation

### What we can access now
Lightweight public dental screening image datasets that are free for academic use, containing labeled healthy and decayed tooth samples.

### What still needs confirmation
- The exact number of valid samples available
- Image resolution and quality specifications
- Whether supplementary on-scene photo capture is needed for our specific use case

## Three Next Actions

1. Collect and sort out open-source dental image datasets; filter for valid, properly labeled samples
2. Define clear classification standards (healthy / early decay / obvious decay) for model training
3. Clean and preprocess image data to unify basic image specifications (resolution, lighting normalization)
