
# News Recommender with Best_Matched_Alt_Topic (v4)

This Flask app returns 6 preferred and 2 serendipitous news articles, with updated logic based on `Best_Matched_Alt_Topic`.

## POST Request

```json
{
  "preferred": 1,
  "non_preferred": 3
}
```

## Serendipitous Logic (Updated)

- `Primary Topic` = Non-Preferred
- `Internal Topic` = "Hybrid"
- `Best_Matched_Alt_Topic` = Preferred
- Sorted by Relevance_{Preferred}, top 5% → randomly pick 2

## Fields Returned

- Prefer_Article[1–6]_{Title, Summary, Topic, Picture}
- Seren_Article[1–2]_{Title, Summary, Topic, Picture}
- Today

## Deployment

Upload with `Enhanced_Dataset_OpenAI_Simplified_4.xlsx` to GitHub, then deploy to Railway.
