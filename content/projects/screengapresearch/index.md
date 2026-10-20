---
title: "ScreenGapResearch"
description: "A straightforward, token-based workflow for materials researchers to submit compositions and review model usage."
hideMeta: true
---

ScreenGapResearch gives busy materials researchers a clean, functional way to request composition predictions without creating a traditional account or password. They provide their company name and email address, verify their email, and receive a secret token to keep safe and use when submitting jobs or checking usage.

<!--more-->

**Role:** Architect, ML pipeline engineer

**Stack:** FastAPI, Python ML stack, Azure Container Instances, Azure Storage Queues

[Visit the live ScreenGapResearch website](https://www.screengapresearch.com/)

## A simple submission workflow

1. **Request access:** Enter a company name and email address, then verify the email. No traditional account password is needed.
2. **Prepare a submission:** Upload a CSV file in the standard format for the research workflow, with the required `formula` column.
3. **Choose a model:** Run the experimental model, the computational model, or both to compare their predictions.
4. **Receive results:** The job is processed asynchronously, and a results notification is emailed to the submitted address.
5. **Check usage:** Enter the email and secret token on the dashboard to view recent jobs, plan limits, and usage.

The goal is a clean, low-friction experience: researchers can submit a file and select a model without managing another password-based account, while keeping usage information available through their token.

## Processing workflow

CSV submissions are queued for containerized inference, and job results are delivered by email. The dashboard provides a view of recent activity and usage limits.

Predictions are screening estimates, not a substitute for experimental validation or professional scientific judgment.
