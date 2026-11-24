# PrismDraft – AI Content Repurposing Workflow

## About the Project
PrismDraft is an AI-powered content repurposing automation system built using **n8n** and **OpenAI**.

It takes a single article as input and automatically transforms it into multiple platform-ready content formats, saving time and reducing manual content creation work.

## Project Objectives
- Automate content repurposing using AI.
- Generate engaging LinkedIn posts and hashtags.
- Create short X (Twitter) threads.
- Generate newsletter content.
- Store generated content automatically.
- Notify the team when content generation is complete.

## Workflow Overview

The project consists of three main modules:

### 1. Input Integration – Member 1
- Receives article details through an n8n Webhook.
- Accepts the title, author, and article body.
- Uses an Edit Fields node to organize the input data.

### 2. AI Content Generation – Member 2
- Uses OpenAI models through Basic LLM Chain nodes.
- Generates LinkedIn posts, hashtags, and key takeaways.
- Creates an X thread containing 3–5 tweets.
- Generates newsletter subject, preheader, email body, and executive summary.
- Uses Structured Output Parsers to maintain structured responses.
- Combines the generated outputs using Merge nodes.

### 3. Output & Delivery Integration – Member 3
- Stores generated content in Google Sheets.
- Creates a Gmail draft containing newsletter content.
- Sends a notification to the team's Slack channel.

## Technologies Used
- n8n – Workflow automation
- OpenAI – AI-powered content generation
- Google Sheets – Content storage
- Gmail – Newsletter draft creation
- Slack – Team notifications
- Webhooks – Input integration

## Workflow Process

1. An article is submitted through the Webhook.
2. The input data is extracted and organized.
3. AI generates content for different platforms.
4. Structured outputs are combined.
5. Generated content is stored in Google Sheets.
6. A newsletter draft is created in Gmail.
7. A completion notification is sent to Slack.

## Key Features
- Automated content transformation.
- Multiple content formats from one article.
- Structured AI-generated outputs.
- Automatic Google Sheets storage.
- Gmail draft generation.
- Slack team notifications.

## Important Note
PrismDraft generates platform-ready content but does not automatically publish posts to LinkedIn or X. Newsletter content is saved as a Gmail draft and is not automatically sent.

## Project Goal
To simplify content repurposing by combining AI and workflow automation into one integrated system.
