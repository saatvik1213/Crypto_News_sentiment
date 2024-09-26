
# Crypto News Sentiment Analysis

This project analyzes the sentiment of cryptocurrency news headlines fetched from the CryptoPanic API and provides an overall average market sentiment score. The sentiment is classified into **positive**, **neutral**, and **negative** categories, and the project outputs a summary of the sentiment distribution along with an overall market sentiment score.

## Features

- **Fetch Real-Time News**: Retrieves the latest cryptocurrency news headlines using the [CryptoPanic API](https://cryptopanic.com/developers/api/about).
- **Sentiment Classification**: Uses a pre-trained machine learning model to classify news into positive, neutral, and negative sentiments.
- **Market Sentiment Calculation**: Computes an average sentiment score based on recent news to help understand the overall market trend.
- **Configurable Parameters**: You can customize the news filter to get specific categories like "bullish," "bearish," "important," etc.

## Installation

To run the project, ensure you have the following Python libraries installed:

```bash
pip install requests numpy keras
```

## API Setup

1. Visit [CryptoPanic](https://cryptopanic.com/developers/api/about) and obtain an API key.
2. Replace the `api_key` variable in the script with your personal API key.

## How It Works

1. The script uses the **CryptoPanic API** to fetch recent cryptocurrency news.
2. The title of each news article is passed to a pre-trained sentiment analysis model.
3. The model classifies each headline into one of three sentiment categories:
   - **Positive**: Bullish market sentiment
   - **Neutral**: No strong market signal
   - **Negative**: Bearish market sentiment
4. The script calculates the percentage of each sentiment and computes an **average sentiment score** between `-1` and `1`, where:
   - `-1` means completely negative sentiment.
   - `1` means completely positive sentiment.
   - `0` indicates neutral sentiment.

## Usage

To run the script, execute the following command:

```bash
python Crypto_News_Sentimental_Analysis.ipynb
```

### Example Output

```
Total Posts Analyzed: 50
Positive: 20 (40.00%)
Neutral: 15 (30.00%)
Negative: 15 (30.00%)
Average Sentiment Score: 0.10
```

In this example:
- **40%** of the news articles had a positive sentiment, indicating a slightly bullish trend.
- The **average sentiment score** of `0.10` suggests a moderately positive outlook in the market.

## Customization

- **Filter News**: Adjust the API query parameters to filter news based on different sentiments or categories (e.g., `bullish`, `bearish`, `important`).
- **Model Customization**: You can replace the pre-trained model with your own model trained on cryptocurrency-specific data for improved sentiment analysis.

## Contributing

Feel free to submit pull requests or open issues for any improvements or bugs.

## License

This project is licensed under the Apache 2.0 License.

---
