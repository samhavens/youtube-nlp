# YouTube NLP

This library takes a CSV of the data of a collection of youtube videos, and, given an example string, finds the "nearest" youtube video.

## Running

If the notebook in this repo is giving you trouble, use the [colab notebook](https://colab.research.google.com/drive/1NRKXK6Ut7gG1-5QbKlrvl0o0UMq9UDol). You just need to upload the CSV file into the notebook when using colab. If running locally, you'll want to modify that slightly.

## Analysis

Currently: high recall, low precision.

The current method worked ok-ish. Using the inner product as a confidence isn't good enough... Sometimes 0.6 means good match, other times not.

## Plans

* Compare to a simpler model  (TFIDF, word2vec)
* Don't concatenate all text fields. Instead, match against title, description, tags, captions separately. Weight different matches by importance.
* Preprocess text... lots of garbage tags and "subscribe to us!!!" messages muddying the signal.

