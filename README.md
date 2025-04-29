# ctc-ml-comparison
## 🚀 Quick Setup & Run

Open a terminal and paste everything below:

## 🚀 Quick Setup & Run

Open a terminal and paste the whole block:

```bash
# 1) Clone repo and enter directory
git clone https://github.com/lyricalbants/ctc-ml-comparison.git && \
cd ctc-ml-comparison

# 2) Create venv and install requirements
python3 -m venv venv && \
source venv/bin/activate && \
pip install -r requirements.txt

# 3A) Launch interactive Jupyter Lab (recommended)
jupyter lab

# 3B) —or— programmatically execute all notebooks and save outputs
mkdir -p executed
for nb in 01_extract_images.ipynb 02_explore_and_augment.ipynb 03_baseline_models.ipynb 04_cnn_training.ipynb; do
  jupyter nbconvert \
    --ExecutePreprocessor.timeout=600 \
    --to notebook \
    --execute "$nb" \
    --output "executed/$nb"
done

