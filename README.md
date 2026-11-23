# eeg-motor-imagery-decoder

Project goal: Decoding imagined movements (left hand, right hand, feet, tongue) from EEG data using BCI Competition IV 2a dataset. The overall goal is to build and compare decoders for 4-class motor imagery, with evaluation that prevents data leaks.

## Plan
- [x] Load data with MNE-Python and inspect channels, sampling rate and trials per class
- [x] Band-pass filter (8–30 Hz) and visualize motor cortex channels (C3, Cz, C4)
- [ ] Epoch trials around imagery cues
- [ ] Baseline: CSP + LDA with cross-session evaluation (train on session T, test on session E)
- [ ] EEGNet in PyTorch
- [ ] Per-subject analysis and failure cases

## Data
[BCI Competition IV download page](https://www.bbci.de/competition/iv/download)
(dataset 2a)

## Setup
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt ipykernel