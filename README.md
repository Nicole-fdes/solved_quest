from textblob import TextBlob

def analyze_sentiment(text):
    # Analyze the sentiment of the text
    analysis = TextBlob(text)
    # Get polarity (-1 to 1) and categorize sentiment
    polarity = analysis.sentiment.polarity
    if polarity > 0:
        sentiment = "Positive"
    elif polarity == 0:
        sentiment = "Neutral"
    else:
        sentiment = "Negative"
    return sentiment, polarity

# Example usage
if __name__ == "__main__":
    # Input text
    text = input("Enter the text for sentiment analysis: ")
    sentiment, polarity = analyze_sentiment(text)
    print(f"Sentiment: {sentiment}")
    print(f"Polarity Score: {polarity:.2f}")
