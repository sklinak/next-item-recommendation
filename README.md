# Next Item Recommendation

A simple recommendation system that predicts the next item
a user will view based on their browsing history.

Built as a university selection assignment for a RecSys & AI track.

## How it works

Builds a transition graph between items: counts how often users
moved from one item to another across all sessions.
To make a prediction — takes the last viewed item and returns
top-10 items that were most frequently viewed after it.

## Data

Synthetic e-commerce dataset — 2565 browsing sessions, 400 unique items.
Each session is a sequence of item IDs in viewing order.

## Usage

1. Place `sessions.jsonl` in the same folder as the notebook
2. Open `recsys_solution_1.ipynb` in Jupyter
3. Run all cells top to bottom

Dependencies: Python standard library + matplotlib only.

## Results

| Model | Hit@10 |
|---|---|
| Top-10 popular items (baseline) | 0.384 |
| **Transition graph (our model)** | **0.514** |

The model correctly predicts the next item in 51% of cases —
13 percentage points better than the simple baseline.
