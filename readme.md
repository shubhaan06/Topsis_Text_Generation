# TOPSIS for Text Generation Model Selection

## Overview
This repository applies the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method to rank pre-trained text generation models based on multiple performance criteria.

## Dataset
The dataset consists of five text generation models evaluated on four criteria:
- **Perplexity** (Lower is better)
- **BLEU Score** (Higher is better)
- **Inference Time** (Lower is better)
- **Memory Usage** (Lower is better)

### Sample Data Table
| Model    | Perplexity | BLEU Score | Inference Time (s) | Memory Usage (GB) |
|----------|------------|------------|------------------|----------------|
| GPT-3.5  | 15         | 0.65       | 0.5              | 4              |
| GPT-4    | 10         | 0.75       | 0.7              | 6              |
| LLaMA 2  | 12         | 0.70       | 0.6              | 5              |
| T5       | 20         | 0.60       | 0.4              | 3              |
| BART     | 18         | 0.55       | 0.8              | 7              |

## Methodology
1. **Normalization**: The decision matrix is normalized using vector normalization.
2. **Weighting**: Each criterion is assigned a weight.
3. **Ideal & Anti-Ideal Solutions**: The best and worst values for each criterion are identified.
4. **Separation Measures**: The distance of each model from ideal and anti-ideal solutions is computed.
5. **Relative Closeness**: A score is calculated for each model.
6. **Ranking**: Models are ranked based on their relative closeness to the ideal solution.

## Installation & Dependencies
Ensure you have the following Python libraries installed:
```bash
pip install numpy pandas matplotlib seaborn
```

## Running the Code
Run the following command in your terminal:
```bash
python topsis_text_gen.py
```

## Output
- A CSV file (`topsis_results.csv`) containing the final rankings.
- Two visualization plots:
  - `ranking_bar_chart.png`: A bar chart showing the ranking of models.
  - `correlation_heatmap.png`: A heatmap of the criteria correlation.

## Results
The output includes a sorted ranking of the models based on their performance using TOPSIS. The best model is ranked highest.

## Contributors
Developed by [Your Name].

## License
This project is licensed under the MIT License.