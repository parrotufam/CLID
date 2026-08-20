# CLID — Controlled Low-Light Image Dataset

CLID (Controlled Low-light Image Dataset) is a dataset for low-light image enhancement research in which illumination is treated as an **explicitly controlled variable** during image acquisition, rather than being simulated through exposure manipulation or synthetic degradation. It provides physically grounded low-light images paired with reference images captured under full illumination, enabling reproducible, fine-grained analysis of how specific lighting factors affect image quality and enhancement algorithm performance.

## Dataset Description

- **1250 pairs** of high-resolution RGB images
- **125 distinct scenes**, each captured under multiple lighting configurations
- Each low-light image is paired with a corresponding **reference image** acquired under full or near-optimal illumination
- Captured resolution: **2400×1344 px** (JPEG); a resized **600×336 px** version is also provided for faster training
- Split: **80% training / 20% validation**, randomly assigned with no overlap between sets
- Scenes combine varied objects, materials (glass, metal, plastic, fabric, paper, organic surfaces), textures, and depth planes to ensure visual diversity while keeping framing and composition consistent across illumination changes

## Acquisition Setup

- **Lighting system:** SpectriWave® Manual Reflective Lighting system, providing independent control over illumination parameters
- **Light source types:**
  - **INC** (Incandescent) — warm illumination
  - **CWF** (Cool White Fluorescent) — office/laboratory-style illumination
- **Controlled parameters** (varied independently, not mixed within a single acquisition):
  - Illumination intensity: levels **20, 40, 70, 100** (INC) and **35, 50, 75, 100** (CWF)
  - Number of active light sources: **4, 8, 16** lamps (INC) and **2, 4, 6** lamps (CWF)
- **Environment:** fully blacked-out indoor setting for precise lighting control
- **Camera:** Canon EOS Rebel SL3, tripod-mounted, wireless remote trigger (no mechanical disturbance)
- Automatic camera corrections disabled and white balance fixed manually to avoid compensating for illumination changes
- ISO constrained to **100–400** to balance realism and noise control

## Applications

CLID supports controlled benchmarking of low-light image enhancement methods along independent illumination dimensions (light type, intensity, number of sources), as well as other illumination-sensitive computer vision tasks such as recognition, detection, and perceptual quality assessment.
