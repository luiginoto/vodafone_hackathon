# Vodafone Data Science Hackathon 2021

This repository contains the submitted project notebook and workflow for Vodafone Data Science Hackathon 2021, organized by Bocconi University and Vodafone Italy (3rd place out of 40 teams). The goal of the challenge was to predict the reason for contact of customer interactions with Tobi, Vodafone's frontline digital assistant (text and voice chatbot), using a supervised classifier.\

## Data description

Each interaction with Tobi is labelled with one of these 4 broad topics: active products, commercial offers, spend management, current balance. Thus, the categorical label to predict is multi-class with 4 classes.\
The dataset contains for each customer the relevant events leading to the interaction with Tobi.
Each record in the provided dataset is one such event and contains:
1. Session identifier: identifies uniquely a Tobi interaction <customer, timestamp,
label> and all events leading up to it
2. Customer identifier
3. Event timestamp
4. Event descriptor: up to four properties for each event, split in distinct columns
o event_category_lv1 o event_category_lv2 o event_category_lv3 o event_category_lv4
5. Tobi session timestamp: the timestamp of the closest future Tobi session
6. Tobi session label: the label of the closest future Tobi session
The last event of a session is the padding: a fictitious event where the descriptor is the number of days until the Tobi interaction.\
Thus, data is provided in long-format, i.e. multiple rows for each labelled data point, with extra properties on the columns.
