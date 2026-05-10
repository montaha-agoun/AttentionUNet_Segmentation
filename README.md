# AttentionUNet_Segmentation

## Acknowledgments  
* Dataset provided by Mateusz Buda and colleagues via The Cancer Imaging Archive (TCIA).
* Architecture inspired by "Attention U-Net: Learning Where to Look for the Pancreas" (Oktay et al., 2018).
[paper-link]: https://arxiv.org/abs/1804.03999
  
## Architecture
The model implements the Attention Gate mechanism proposed by Oktay et al. (2018). These gates filter the features passed through skip connections using a gating signal from coarser (deeper) scales.
* **Input:** $256 \times 256$ RGB MRI slices.
* **Output:** Binary segmentation mask (Logits).
* **Optimization:** Adam optimizer with a $10 \times$ smaller learning rate for the pretrained encoder.

## Results 
 * Loss   : 0.7589
 * Dice   : 0.9023
 * IoU    : 0.8736
