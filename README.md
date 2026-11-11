# Event-Driven Sentiment Analysis of Indian Audiences Towards Muslim Content Creators

A course project on how sentiment and toxicity in YouTube comments change around major geopolitical events in India, built with **Python** and **VADER**.

**Group project.** The proposal is by Sakshi Borekar, Nishi, Diya and Manish (Azim Premji University). The poster is by Sakshi Borekar.

**My role:** I did the **programming and coding work** in **Python**: collecting comments with the **YouTube Data API**, cleaning and structuring the data with **Pandas**, scoring sentiment with **VADER**, building the **rule-based toxicity and theme classification**, and running the **pre-event and post-event comparison**. The final notebook is not included in this repository yet. For now it holds the proposal and the poster.

## Research question
How do Indian audiences' sentiments towards Muslim content creators change over time following major geopolitical events?

## Hypothesis
Major geopolitical events lead to a measurable increase in negative sentiment towards Muslim content creators in the post-event period compared to the pre-event period.

## Data
- YouTube comments and replies from 13 creators (7 Muslim, 6 Hindu) who post non-political content, selected as a randomised sample
- Videos from March to June 2025, collected with the **YouTube Data API** (**google-api-python-client**)
- About 150 comments per creator: roughly 700 for Muslim creators and 600 for Hindu creators
- Raw comments are not included in this repository, to protect commenters' privacy

## Methods and tools
- **Tools:** **Python**, **Pandas**, **google-api-python-client**, **VADER**, **Google Colab**
- Pipeline: data collection, then cleaning (noise removal, timestamp standardisation), then classification, then comparison before and after each event
- **Sentiment analysis:** **VADER**, a lexicon-based method
- **Toxicity and theme detection** (nationalism, religion, politics): **rule-based classification**
- **Time-series analysis** of daily average sentiment and toxicity around the Pahalgam attack and Operation Sindoor, compared between Muslim-creator and Hindu-creator comments

## Key findings
- Sentiment and toxicity spiked around the Pahalgam attack and Operation Sindoor for both creator groups.
- Comments under Muslim creators showed higher short-term volatility; comments under Hindu creators showed a more sustained decline in sentiment.
- Falling sentiment lined up with rising toxicity. Neither measure returned to its March level in the period studied.
- Volatility was sharper in comments about nationalism, religion and politics, and the religion-related volatility appeared longer-lasting.

## Limitations
- YouTube comments only, and a limited set of creators, so the results may not represent the wider audience.
- VADER and rule-based methods can miss sarcasm and mixed-language text.
- The analysis shows trends, not causal relationships.

## Future work
More platforms and creators, a longer time period, better multilingual models and better handling of sarcasm.

## Files
- `docs/Poster-YouTube-sentiment-analysis.pdf`: the project poster, which reports the completed analysis
- `docs/Proposal-YouTube-sentiment-analysis.pdf`: the original proposal, which describes a wider plan (several platforms, 10,000 to 50,000 comments) than the one completed
