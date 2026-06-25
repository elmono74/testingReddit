# testingReddit
# AI Insurance Lead Finder - Reddit API Prototype

This repository is for a small prototype that tests Reddit API access for a human-reviewed social listening dashboard.

## Purpose

The app reads a limited number of publicly available Reddit posts and comments from configured subreddits and displays them in a private review dashboard. The prototype is used to evaluate whether public conversations may indicate general interest in auto insurance topics such as:

- Auto insurance
- SR-22 insurance
- People looking for Pen Pals
- People looking for post card swaps

## What The App Does

- Uses Reddit’s API to read public subreddit posts and top-level comments
- Stores the original text, permalink, timestamp, and source subreddit
- Uses an AI classifier to assign an intent score and category
- Displays possible matches in a private dashboard for human review
- Allows a human reviewer to mark a lead as contacted or dismissed

## What The App Does Not Do

- Does not post to Reddit
- Does not comment on Reddit
- Does not send Reddit messages
- Does not vote
- Does not scrape private content
- Does not bypass login, paywalls, rate limits, or access controls
- Does not automatically contact users
- Does not sell Reddit data
- Does not share Reddit data with advertisers
- Does not use Reddit data for ad targeting

## Reddit API Usage

The app uses Reddit API credentials for server-side testing. API usage is intentionally limited during testing.

Example configuration:

```env
REDDIT_SUBREDDITS=Insurance,carinsurance,SR22
INGESTION_LIMIT_PER_SOURCE=5
