# 1. Set Up Your Environment
## 1.1. Install Homebrew (Optional but Recommended)

Homebrew is a package manager that makes it easy to install and manage many development tools on macOS. If you already have it, skip this step.
Open the Terminal app and run:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 1.2. Install Python 3

```
brew install python
```

Confirm that Python is installed:

```
python3 --version
```

if too old or too new, try:
```
brew install python@3.11
```

## 1.3. Create a Virtual Environment
It’s good practice to create a virtual environment to manage your project’s dependencies.

```
python3 -m venv llm-env
source llm-env/bin/activate
```

to deactivate, use:
```
deactivate
```

## 1.4. Install Required Python Libraries
You’ll need transformers, datasets, and a deep learning backend (e.g. PyTorch) to train or finetune models locally.


pip install --upgrade pip
pip install torch torchvision torchaudio  # or "pip install torch --upgrade" if you only need PyTorch
pip install transformers datasets
pip install accelerate  # For optimized training on Mac M1/M2 or CPU
(As of PyTorch 2.0, macOS (especially Apple Silicon) has improved support for MPS acceleration, which can speed up training.)

