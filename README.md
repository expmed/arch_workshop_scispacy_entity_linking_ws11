# ARCH Workshop: Named Entity Linking from Clinical and Biomedical Text with SciSpacy [WS12]

### Links to Resources used During Workshop

- [SpaCy Package](https://spacy.io/)
- [SciSpaCy Package](https://allenai.github.io/scispacy/)
- [SciSpaCy Github Page](https://github.com/allenai/scispacy)
- [Hugging Face Dataset Link](https://huggingface.co/datasets/AGBonnet/augmented-clinical-notes)

## Options to Follow Along with the Hands On Module

### *Option 1.* Link to Notebook in Google Colab *(preferred)*:
1. Google Colab Link to Notebook: [Google Colab Link](https://colab.research.google.com/github/expmed/arch_workshop_scispacy_entity_linking_ws11/blob/main/workshop_notebook.ipynb)

### *Option 2.* Minimal Local Environment Instructions *(for Workshop Attendees who Want to Run Locally)* 

These steps will help you install Python, set up a Conda environment, fetch the Synthea generator, and run the workshop notebooks locally.

📦 Step 1: Install Anaconda (Recommended)
Anaconda includes Python, Jupyter, and package management tools in one.

Download and install Anaconda for your operating system:

[Windows / macOS / Linux](https://www.anaconda.com/download)

After installing, open Anaconda Prompt (Windows) or a terminal (Mac/Linux).

📂 Step 2: Clone the Workshop Repository
If you're using Git:

```bash
git clone https://github.com/expmed/arch_workshop_scispacy_entity_linking_ws11.git
cd arch_workshop_scispacy_entity_linking_ws11
```
Or, download the ZIP from the provided link and extract it. Then navigate into the folder:

```bash
cd arch_workshop_scispacy_entity_linking_ws11
```
🧪 Step 3: Create and Activate the Conda Environment
This installs all required Python packages for the notebooks.

```bash
conda env create -f environment.yml
conda activate arch_ws_12_env  # replace with your env name if different
```

🔨 Step 4: Install the ScispaCy and HuggingFace Hub packages

***Note: nmslib is a dependency of Scispacy and needs to be installed separately and prior to installing ScispaCy***

- If on Windows 11, you should be able to just do `pip install scispacy` and nmslib should be installed correctly.
- If on an M1 MacOS machine, you should be able to first use `CFLAGS="-mavx -DWARN(a)=(a)" pip install nmslib` followed by `pip install scipsacy`
- If on an M2 - M4 MacOS machine, `conda install -c conda-forge nmslib` followed by `pip install scispacy` should work

Follow the instructions above to install the nmslib dependency, and then execute the following in your activated `arch_ws_12_env` environment

1. Install scispacy with `pip install scipacy`
2. Install the small scispacy model with `pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.5.4/en_core_sci_sm-0.5.4.tar.gz`
3. Install HuggingFace Hub with `pip install huggingface_hub`


📓 Step 5: Launch the Workshop Jupyter Notebook
From within your activated Conda environment and workshop directory:

```bash
jupyter lab
```
Your browser will open automatically. Navigate to the .ipynb files for hands-on exercises. 