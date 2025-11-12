# Fast Goal-Conditioned Diffusion Policy for Real-Time Visuomotor Control

An implementation of a fast, single-step, goal-conditioned policy for visuomotor control. Fast GCDP takes an observation (e.g. RGB) and a goal (e.g. goal image/embedding) and predicts a short horizon of actions in one forward pass, inspired by diffusion-policy distillation / one-step approaches.

Project Page (TBD)

---

## 📋 Requirements
- Python 3.8+
- PyTorch 1.9+ (or newer)
- CUDA-capable GPU (recommended)
- torchvision (if using image encoders)

---

## 🛠️ Installation

Clone the repository:
```bash
git clone https://github.com/gc9616/fast_gcdp.git
cd goalflow
```

Install dependencies:
```bash
pip install -r requirements.txt
```

## 📝 Notes

- Fast-GCDP is meant to be lightweight and easy to slot into an existing robotics stack.

- The model is trained with a straightforward supervised loss (MSE over the predicted horizon).

- You can swap the encoders (e.g. ResNet, ViT, language encoders) without changing the training loop.
