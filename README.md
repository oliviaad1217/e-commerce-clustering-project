# e-commerce-clustering-project
Comparing K-Means, PCA, and autoencoder representations for e-commerce transaction clustering, with evaluation of cluster quality and interpretability.
## Results and Interpretation

The study compared K-Means clustering across different feature
representations. The submitted report records the following results:

| Approach | Number of clusters | Silhouette score |
|---|---:|---:|
| K-Means baseline | 3 | 0.914 |
| PCA + K-Means baseline | 3 | 0.865 |
| Tuned PCA + K-Means | 3 | 0.921 |
| Autoencoder + K-Means baseline | 3 | 0.352 |
| Tuned shallow autoencoder + K-Means | 14 | 0.658 |
| Tuned deep autoencoder + K-Means | 3 | 0.897 |

These are historical results reported in the coursework.
They have not been independently reproduced for this repository.

### Main Findings

- Tuned PCA achieved the highest reported silhouette score,
  slightly exceeding the K-Means baseline.
- Additional neural-network complexity did not consistently improve
  clustering performance or interpretability.
- The baseline produced highly imbalanced clusters: 19,739,
  42, and 7 transactions. Its high silhouette score therefore
  does not establish useful segmentation of typical purchases.
- More granular autoencoder clusters offered additional profiles
  to investigate, but their practical usefulness was not validated.

### Business Interpretation

For this dataset, a simpler approach provided a strong starting point.
More complex models should be justified by stable, interpretable
purchase patterns that could support a specific business decision.

The project did not measure improvements in sales, campaign
performance, or customer retention.

### Evaluation Limitations

Silhouette scores were calculated in different feature spaces,
so comparisons require caution.

The baseline autoencoder branch clusters reconstructed outputs
rather than bottleneck embeddings. This implementation needs
correction and re-evaluation before drawing firm conclusions
about latent-space clustering.

### Next Steps

- Correct the baseline autoencoder representation.
- Test cluster stability across random seeds.
- Evaluate sensitivity to outliers and scaling choices.
- Compare cluster profiles in the original transaction features.
- Validate whether the segments support a practical business use case.
