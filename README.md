# Freshdesk Daily Ticket & SLA Tracker

An automated customer-support reporting workflow built with **n8n**, **Freshdesk**, and **Google Sheets**.

This automation retrieves daily Freshdesk tickets, processes the ticket information, calculates support performance metrics, and records the results in a structured Google Sheet.

## What It Does

* Retrieves Freshdesk tickets created during the current day
* Converts ticket status and priority IDs into readable values
* Identifies the responsible support team
* Records the responsible team members
* Calculates the total number of tickets for the day
* Calculates time taken from ticket creation to resolution
* Determines First Response SLA performance
* Determines Resolution SLA performance
* Identifies whether a ticket was escalated
* Converts Freshdesk Group IDs into readable group names
* Sends the processed data to Google Sheets

## Workflow

Freshdesk → n8n → Data Processing → Google Sheets

The n8n Code node processes the Freshdesk ticket data before sending the final information to Google Sheets.

## Key Metrics

| Metric                | Description                                    |
| --------------------- | ---------------------------------------------- |
| Total Tickets         | Total number of tickets created during the day |
| Time Tracked          | Time between ticket creation and resolution    |
| First Response Status | Whether the first response was within the SLA  |
| Resolution Status     | Whether the ticket was resolved within the SLA |
| Is Escalated          | Indicates whether the ticket was escalated     |
| Responsible Team      | Team responsible for the day's tickets         |
| Group                 | Freshdesk support group handling the ticket    |

## Technologies

* **n8n** — Workflow automation
* **Freshdesk** — Customer support and ticket management
* **Google Sheets** — Daily reporting and data storage
* **JavaScript** — Ticket processing and calculations

## Purpose

The purpose of this project is to automate daily customer-support reporting and eliminate repetitive manual data collection.

Instead of manually reviewing Freshdesk tickets and compiling a daily report, the workflow processes the information automatically and produces a structured report in Google Sheets.
