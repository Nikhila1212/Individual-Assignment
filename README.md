# Attention Mechanisms in Image Captioning
### *Teaching a Network to Look Before It Speaks*


---

## What This Is

A tutorial on **visual soft attention** in neural image captioning, based on the  
*Show, Attend and Tell* architecture (Xu et al., 2015).

The tutorial explains why single-vector CNN encoders lose spatial information,
how the attention mechanism fixes this, the difference between soft and hard attention,
and how this directly connects to modern Transformer self-attention.

**Dataset:** Microsoft COCO Captions (MSCOCO) — 330k images, 1.6M human captions  
**Technique:** Additive (Bahdanau-style) soft attention over CNN feature grids  
**Evaluation:** BLEU-4, CIDEr on MSCOCO test split

---

## Repository Contents

| File | Description |
|---|---|
| `attention_tutorial.docx` | Full tutorial document (Word format, <2000 words) |
| `attention_tutorial.ipynb` | Jupyter notebook — all code, figures, model implementation |
| `README.md` | This file |
| `LICENSE` | MIT licence |

---

## How to Run the Notebook

### Requirements

```bash
pip install numpy matplotlib torch torchvision nbformat
```

PyTorch is optional — if not installed, model definition cells are skipped gracefully  
and all figures still render.

### Run

```bash
jupyter notebook attention_tutorial.ipynb
```

Or open in JupyterLab, VS Code, or Google Colab.

### Google Colab (no local install needed)

Upload `attention_tutorial.ipynb` to [colab.research.google.com](https://colab.research.google.com)  
and run all cells. PyTorch is pre-installed in Colab.

---

## Figures Produced

The notebook generates three figures saved as `.png` files:

- **fig1_attention_heatmap.png** — Attention weight matrix α over caption words × image regions (YlOrBr colourmap — colourblind safe)
- **fig2_architecture.png** — Full Show, Attend and Tell architecture diagram
- **fig3_soft_hard_bleu.png** — Soft vs Hard attention comparison + BLEU-4 training curves (hatch patterns for colourblind safety)

---

## Accessibility

- All figures use colourblind-safe palettes (YlOrBr, hatch patterns on bar charts)
- All images include descriptive alt text in the tutorial document
- Section headings follow a logical H1→H2→H3 hierarchy for screen-reader navigation
- Code blocks use monospace fonts at readable size
- Colour is never the sole means of conveying information

---

## References

1. Xu, K. et al. (2015) *Show, Attend and Tell* — https://arxiv.org/abs/1502.03044
2. Vinyals, O. et al. (2015) *Show and Tell* — https://arxiv.org/abs/1411.4555
3. Bahdanau, D. et al. (2015) *Neural Machine Translation by Jointly Learning to Align and Translate* — https://arxiv.org/abs/1409.0473
4. Anderson, P. et al. (2018) *Bottom-Up and Top-Down Attention* — https://arxiv.org/abs/1707.07998
5. Vaswani, A. et al. (2017) *Attention Is All You Need* — https://arxiv.org/abs/1706.03762
6. Lin, T.Y. et al. (2014) *Microsoft COCO* — https://arxiv.org/abs/1405.0312

---

## Licence

MIT — see [LICENSE](LICENSE). You are free to use, adapt, and share this tutorial with attribution.
