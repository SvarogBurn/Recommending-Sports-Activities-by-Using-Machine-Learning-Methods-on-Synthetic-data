# Sports Activity Recommendation: Thesis Data and Outputs

Storage for the datasets and analysis outputs from my BSc thesis, *Recommending Sports Activities Using Synthetic Data Generation and Machine Learning* (Faculty of Informatics and Digital Technologies, University of Rijeka, 2025).

This repository is a data appendix, not a runnable project. It holds the inputs and the results, not the analysis scripts. The point is to keep the thesis data in one place and make it easy to reference.

## What the thesis was about

The work looks at the cold-start problem in recommender systems. A new platform has no interaction history, so there is nothing for a recommender to learn from. The question was whether synthetic data can stand in for real data long enough to bootstrap the system, and where that substitution breaks down.

The approach, in short:

- Two datasets were built from a review of more than 50 papers: 90 sports described by 51 attributes, and 1,000 synthetic users described by 18 attributes, plus a user and sport interaction set.
- Exploratory Factor Analysis reduced the raw attributes to interpretable factors, for both users and sports.
- K-Means and HDBSCAN segmented users and sports into groups.
- The synthetic clustering was compared against real-data structure using the Adjusted Rand Index. The thesis records the cases where synthetic data did not reproduce the real preference structure, which is the more useful finding.

## Files

| File | What it holds |
|------|---------------|
| `UsersDataset.csv` | Synthetic user profiles (1,000 users, 18 attributes) |
| `SportsDataset.csv` | Sports and their attributes (90 sports, 51 attributes) |
| `InteractionsDataset.csv` | User and sport interaction records |
| `user_factor_scores.csv`, `sports_factor_scores.csv` | Factor scores from the EFA |
| `user_attribute_factor_loadings.csv`, `sport_attribute_factor_loadings.csv` | Factor loadings from the EFA |
| `user_cluster_centroids.txt` | K-Means cluster centroids for users |
| `sport_hdbscan_clustering_report.txt` | HDBSCAN clustering report for sports |

## Note on the code

The analysis scripts are kept separately and are not part of this repository. If you want to see the methods rather than the results, the thesis document itself describes the full pipeline.

## Related work

Co-authored paper, *Analyzing Social Networks of Sport Preferences for Personalized Recommendations*, presented at MIPRO 2025. Both came out of the MoveUs project.
