# 7PAVNLPS

## Beyond F1: biomedical sentence classification and robustness

Original coursework notebook for PubMed RCT sentence-role classification. It compares lexical, position-aware, sequence and transformer methods, with perturbation-based behavioural evaluation, uncertainty analysis and a PubMed RCT 200k cross-scale layer.

The five sentence roles are Background, Objective, Methods, Results and Conclusions. The notebook includes numeric, paraphrase, structure and negation perturbations. Its own methodological qualifications apply: negation response is not correctness without manual expected labels, and capped 200k neural/transformer runs are exploratory.

## Files

- `AG16013_7PAVNLPS_JupyterNotebook.ipynb`: the supplied notebook, preserved byte for byte, including saved outputs and metadata.
- `requirements.txt`: dependencies identified in notebook imports. The supplied file does not specify a complete package lock; these are not claimed to reproduce its original environment exactly.
- `SOURCE_MANIFEST.json`: source identity, SHA-256 and notebook cell counts.

## Run

1. Open the notebook in Google Colab or a Jupyter environment. Install Jupyter separately if running locally, then install the dependencies with `pip install -r requirements.txt`.
2. Supply the PubMed RCT data independently. The notebook initially expects `train.txt`, `dev.txt` and `test.txt` under `/content/drive/MyDrive/`; update its `DATA_DIR` for another location.
3. For the 200k sections, inspect the paths in those cells. They reference `PubMed_RCT_200k_extracted/train200k.txt`, `dev200k.txt`, `test200k.txt` and a `train200k.7z` archive under Google Drive. Archive extraction also needs a compatible 7-Zip command in the runtime.
4. Review the publication/debug switches and model settings, then run cells in order. Transformer and neural training benefits from a suitable GPU and requires model downloads.

Saved outputs belong to the supplied execution. Importing this repository did not rerun training or independently validate the reported results. No dataset or model weights are bundled.

## Source fidelity

No notebook cell, algorithm, result, output or metadata was edited during repository preparation. Only repository documentation, the dependency list, ignore rules and source manifest were added. SHA-256 in the manifest permits checking the original file.
