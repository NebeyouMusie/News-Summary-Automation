# News Summary Automation with n8n

Automate your news consumption with AI-powered summaries! This project extracts articles from RSS feeds, processes them through AI for concise summarization, and stores the results in Airtable for easy access and review.

![News Summary Automation Cover](./images/News%20Summary%20Automation.png)

---

## Table of Contents

- [Overview](#overview)
- [How It Works](#how-it-works)
  - [Workflow Steps](#workflow-steps)
- [Benefits](#benefits)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
  - [1. Clone or Import Workflow](#1-clone-or-import-workflow)
  - [2. Configure RSS Feeds](#2-configure-rss-feeds)
  - [3. Connect Gemini AI](#3-connect-gemini-ai)
  - [4. Connect Airtable](#4-connect-airtable)
  - [5. Customize Summary Parameters](#5-customize-summary-parameters)
  - [6. Schedule the Trigger](#6-schedule-the-trigger)
  - [7. Test the Workflow](#7-test-the-workflow)
- [Customization](#customization)
  - [RSS Feed Configuration](#rss-feed-configuration)
  - [AI Summary Customization](#ai-summary-customization)
  - [Airtable Structure](#airtable-structure)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

---

## Overview

**News Summary Automation** is an n8n workflow designed for content creators, researchers, and news enthusiasts. It:

- Automatically fetches articles from multiple RSS feeds
- Processes content through Gemini AI for intelligent summarization
- Converts HTML content to clean Markdown format
- Stores structured summaries in Airtable for easy access and organization
- Runs on a scheduled basis to keep you updated with the latest news

---

## How It Works

![News Summary Workflow](./images/News%20Summary.png)

### Workflow Steps

1. **Scheduled Trigger**
   - Initiates the workflow at regular intervals (configurable timing)

2. **Fetch RSS Feeds**
   - Retrieves a predefined list of RSS feeds from the workflow code
   - Supports multiple news sources and content types

3. **Loop Through Feeds**
   - Iterates through each RSS feed to process articles individually
   - Ensures comprehensive coverage of all configured sources

4. **Read Latest Articles**
   - Extracts the most recent articles from each feed
   - Captures article content, titles, URLs, and publication dates

5. **AI Summarization with Gemini**
   - Sends article content to Gemini AI for intelligent analysis
   - Generates concise, informative summaries while preserving key insights

6. **HTML to Markdown Conversion**
   - Converts HTML content to clean Markdown format
   - Improves readability and makes content easier to process

7. **Structure and Save to Airtable**
   - Organizes summary outputs with metadata
   - Stores records in Airtable for centralized access and management

---

## Benefits

- **Saves time** reading full articles while maintaining understanding
- **Delivers clear, concise insights** through AI-powered analysis
- **Centralizes summaries** for easy access and reference
- **Enhances content understanding** with intelligent AI assistance
- **Automates news consumption** for busy professionals
- **Maintains historical record** of summarized content

---

## Requirements

- [n8n](https://n8n.io/) installation or cloud account
- Google account with access to Gemini AI API
- Airtable account and base for storing summaries
- RSS feeds you want to monitor and summarize

---

## Setup Instructions

### 1. Clone or Import Workflow

- Download or import the attached `News Summary.json` workflow in your n8n instance
- Use the Visual editor or Desktop version for easy setup

### 2. Configure RSS Feeds

- Edit the RSS feed list in the workflow code
- Add your preferred news sources and content feeds
- Ensure RSS URLs are accessible and properly formatted

### 3. Connect Gemini AI

- Add your Google/Gemini AI credentials in n8n
- Configure the AI node with your preferred model settings
- Set appropriate rate limits and API quotas

### 4. Connect Airtable

- Add your Airtable credentials to the workflow
- Configure the base ID and table name for storing summaries
- Ensure proper permissions for creating and updating records

### 5. Customize Summary Parameters

- Adjust the AI prompt for desired summary length and style
- Configure content filtering preferences
- Set summary quality and relevance thresholds

### 6. Schedule the Trigger

- Configure the schedule node for your preferred run frequency
- Consider news update patterns and your reading schedule
- Daily or hourly triggers are recommended for news content

### 7. Test the Workflow

- Run the workflow manually to verify all connections
- Check Airtable for properly formatted summary records
- Monitor AI processing and content quality

---

## Customization

### RSS Feed Configuration

Configure your RSS feeds by editing the workflow code:

```javascript
// Example RSS feed configuration
const rssFeeds = [
  "https://feeds.bbci.co.uk/news/rss.xml",
  "https://rss.cnn.com/rss/edition.rss",
  "https://feeds.reuters.com/reuters/topNews"
];
```

### AI Summary Customization

Customize the Gemini AI prompt for different summary styles:

**Concise Summary**: "Provide a 2-3 sentence summary of the key points in this article."

**Detailed Analysis**: "Summarize this article in 4-5 sentences, highlighting main arguments and supporting evidence."

**Business Focus**: "Extract the key business insights and market implications from this article."

### Airtable Structure

Your Airtable base should include these columns for optimal organization:

![Airtable News Table Example](./images/Airtable%20News%20Table.png)

- **Title**: Article headline
- **Summary**: AI-generated summary content
- **Link**: Original article link
- **Published Date**: Article publication timestamp
- **Category**: Content classification (optional)
- **Keywords**: Extracted key terms (optional)

---

## Troubleshooting

- **RSS feed errors**: Verify feed URLs and accessibility
- **Gemini AI failures**: Check API quotas and authentication
- **Airtable connection issues**: Verify credentials and table permissions
- **Content processing errors**: Review HTML parsing and AI prompt formatting
- **Workflow scheduling problems**: Check n8n instance status and cron expressions

---

## Contributing

Contributions and suggestions are welcome!  
Fork the repo, submit issues, or create pull requests for workflow improvements.

---

## License

This project is licensed under the MIT License.

---

## Contact

- **Email:** nebeyoumusie@gmail.com
- **LinkedIn:** [LinkedIn](https://www.linkedin.com/in/nebeyou-musie)
- **X(Twitter):** [X](https://x.com/NebeyouMusie)
- **Upwork:** [Upwork](https://www.upwork.com/freelancers/~017ff01729e3cd26e0?mp_source=share)
- **My Agency:** [Fuzion Tech Website](https://fuzion-tech.com/) or [Fuzion Tech on Upwork](https://www.upwork.com/agencies/1948388369189366041/)

---

**Skills & Technologies:**  
`n8n`, `Automation`, `RSS`, `Gemini`, `Airtable`

---

**Enjoy automated news consumption and AI-powered insights!**

---

> _For any issues, please contact the project maintainer or open an issue on your workflow repository.
