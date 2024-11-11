# New Knowledge Datasets

Each CSV file in this directory contains evaluation data with the following core columns:
- `id`: Unique identifier for each example
- `prompt`: The input prompt/question
- `answer`: The expected answer/response

Individual datasets also contain additional columns specific to their evaluation criteria and domain.


# Updating Knowledge Datasets
The updating knowledge datasets are structured slightly differently, namely that we need the un-updated facts to identify which the model already knows.
Each Parquet file contains evaluation data with the following core columns:
- `id`: Unique identifier for each example
- `prompt`: The input prompt/question
- `answer`: The expected answer/response

Additionally, the `*_generalization.csv` file will contain a column called `answer_before`, which is the correct answer prior to the update being made.
This column is used to identify which facts are located in the model's knowledge (such that the update is a true update rather than new knowledge)

The `*_generalization.csv` file also contains contextual information where the updates were taken from.
