# Streptomyces-interaction-networks
Minimal PyTorch Geometric notebook that turns a 60×60 bacterial-interaction adjacency matrix into a graph auto-encoder. Trains a 2-layer GCN (Graph Convolutional Network) encoder, learns node embeddings, clusters with k-means, plots latent space. Drop in any square CSV (Comma-Separated Values), run, adapt, reuse.


## Repo layout

```
.
├── data/
│   └── bacterial_interactions_60x60.csv    # demo adjacency matrix
├── notebooks/
│   ├── 01_eda.ipynb                        # exploratory data analysis
│   ├── 01_eda.html                         # HTML export for quick view
│   └── 02_gnn_bacterial_matrix.ipynb       # GAE workflow
├── environment.yml                         # Conda spec
├── LICENSE                                 # MIT
└── README.md
```

## Quick start

```bash
conda env create -f environment.yml
conda activate bacterial-gnn
# Inspect the data
jupyter lab notebooks/01_eda.ipynb
# Train the GNN
jupyter lab notebooks/02_gnn_bacterial_matrix.ipynb
```

CPU runtime ≈2 min; GPU ≈20 s.

## Adapting

* Swap the CSV for any square adjacency matrix.
* Provide real node features by editing `data.x` in *Cell 3* of `02_gnn_bacterial_matrix.ipynb`.
* Tune cluster count `k` via silhouette or elbow methods.

## License

Released under the **MIT License** — free use, modification, and distribution with attribution.
