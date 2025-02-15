# Pivot Table Automation: Semantic Matching Research

## Summary

This project focuses on creating an automated system for generating pivot tables by matching rows from two different tables based on their semantic similarity. The goal is to develop a solution that can accurately identify rows with similar meaning and then generate a pivot table from them. To achieve this, I researched and compared different algorithms for semantic string matching, including **RapidFuzz**, **Jaccard Index**, and **CrossEncoder**. The performance of each algorithm was evaluated based on its ability to match strings with similar meanings.

## Motivation

The need for this research arose from the requirement to automate the creation of pivot tables with a high level of accuracy. The client requested a nearly perfect pivot table, which necessitated an effective semantic matching approach to match rows meaningfully. Given that the vocabulary in the dataset was highly specific, achieving accurate matching without extensive historical data proved challenging.

## Approach & Results

I evaluated various semantic similarity algorithms to find the most effective solution:

- **RapidFuzz**: This algorithm demonstrated the best performance in terms of speed and accuracy for string matching.
- **Jaccard Index**: This approach showed reasonable results but lacked the precision needed for complex and contextually nuanced data.
- **CrossEncoder**: While promising, this model didn’t perform as expected for this specific task.

I also attempted to fine-tune a **reBERT** model for better semantic understanding, but it didn't yield the desired results due to the insufficient size of the available dataset and the highly specific vocabulary.

### Conclusion

Based on the research findings, **RapidFuzz** proved to be the most effective algorithm for semantic string matching in this scenario. However, the client’s requirement for near-perfect pivot tables highlighted a key limitation: more **historical data** is needed to ensure optimal performance, as the specific vocabulary used in the dataset requires a deeper understanding that can only be achieved through additional training on a larger, more diverse dataset.

## Future Work

To achieve even better results, I recommend expanding the dataset to include more historical data and retraining models such as **reBERT** for more accurate semantic matching. This will improve the robustness and accuracy of the pivot table generation process.
