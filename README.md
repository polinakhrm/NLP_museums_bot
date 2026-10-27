# Bologna Museum Assistant

Bologna Museum Assistant is a small chatbot created with Google Dialogflow CX for an NLP course project.
The chatbot helps tourists discover some of the main museums in Bologna and provides recommendations and practical visitor information.

## Supported Museums

The assistant currently supports:

- MAMbo – Museum of Modern Art of Bologna
- Museo Morandi
- Pinacoteca Nazionale di Bologna
- Museo Civico Archeologico
- Teatro Anatomico

## Features

The chatbot can:

- provide information about museums and their collections;
- recommend a museum based on the user's interests;
- recommend museums based on the user's available time;
- compare different museums;
- provide practical information such as opening hours and ticket prices;
- provide museum contact information;
- remember conversational context for follow-up questions;
- personalize the conversation using the user's name.

## Intents

The following intents are used to recognize the main types of user requests:
- Default Welcome Intent – starts the conversation;
- capture.name – captures the user's name;
- museum.information – handles general questions about museums;
- museum.recommendation – handles museum recommendations based on interests;
- museum.recommendation_by_time – handles recommendations based on available time;
- museum.practical_info – handles questions about opening hours, tickets and other practical information;
- museum.comparison – handles comparisons between museums;
- museum.contacts – provides museum contact information;
- Default Negative Intent – provides negative training examples for intent recognition.

## Entities

The project uses both custom and system entities.
Custom Entities
- `@museum` – identifies the supported museums and their alternative names.
- `@interest` – identifies user interests.

## System Entity
- `@sys.person` – extracts the user's name for conversation personalization.
- `@sys.date` – identifies dates mentioned by the user for visit planning.
- `@sys.time` – identifies time expressions used for museum recommendations and opening-hours queries.
  
## Architecture

The chatbot combines traditional Dialogflow CX functionality with generative AI.

Dialogflow intents and entities are used to identify common user requests and important information such as museum names and interests.

A Dialogflow CX Playbook is used for more flexible conversations, recommendations, comparisons, follow-up questions, and response generation.
