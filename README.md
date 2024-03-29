# NLP-with-Transformers
A code implementation based on the book NLP with Transformers by Lewis Tunstall

## Introduction to Transformers
### Taken an exerpts from an research paper's abstract and trialed different pipelines with distinct intput models and hyperparameters. Overall, the default semantic analysis model doesn't work quite well with text inputs from the research paper.

text = """We aim to develop methods for understanding how multimedia news exposure can affect people’s emotional responses, \
and we especially focus on news content related to gun violence, a very important yet polarizing issue in the US \
We created the dataset NEmo+ by significantly extending the US gun violence news-to-emotions dataset \
BU-NEmo, from 320 to 1,297 news headline and lead image pairings and collecting 38,910 annotations in a large crowdsourcing experiment. \
In curating the NEmo+ dataset, we developed methods to identify news items that will trigger similar versus divergent emotional responses. \
For news items that trigger similar emotional responses, we compiled them into the NEmo+- Consensus dataset \
We benchmark models on this dataset that predict a person’s dominant emotional response toward the target news item (single-label prediction)."""

![image](https://user-images.githubusercontent.com/80212154/230265848-8c43230a-e838-4442-ace9-5bd4a97f66fa.png)
The model predicts the input as negative mood, however, it should be neutral or even positive based on human standard;

![image](https://user-images.githubusercontent.com/80212154/230266516-cfc8c6c5-60e8-4767-a346-19e16f584f6e.png)
trialed tokenization categorization with different aggregation_strategy including first, average, max and simple. None provides optimal results

Text Summarization provides result that's close to meaning of the input.

Trialed text translation from english to chinese with model = "liam168/trans-opus-mt-en-zh";

![image](https://user-images.githubusercontent.com/80212154/230267075-97401806-97eb-4502-988c-e804b39f5ab6.png)
text generation provides results relavent to the emotions of the texts;Since default pipeline is based on emotion classification;
