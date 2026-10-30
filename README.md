# Issue Tracker Form

A small browser form for collecting support issues and posting their details to a Google Apps Script endpoint. This repository contains the frontend only.

## Purpose and implementation

The form captures an issue summary, description, actions taken, and support link. Plain JavaScript serializes the fields as URL-encoded form data, submits a POST request, and displays success or failure feedback. A successful HTTP response resets the form.

**Stack:** HTML, inline CSS, browser JavaScript, Fetch API.

## Preview locally

Clone this repository and open `index.html` in a browser. No package installation or build step is required.

Before submitting any information, replace the Apps Script URL in `index.html` with a deployment you control. The existing destination belongs to the original setup.

## Connect a backend

Deploy your own Google Apps Script web app with a POST handler for these fields:

- `summary`
- `description`
- `actions`
- `supportLink`

Implement storage and response handling in that separate service, then test browser access and cross-origin behavior using synthetic data.

## Current scope

This is a frontend integration prototype. The Apps Script source, spreadsheet schema, authentication, issue list, and status-management workflow are not included. A successful HTTP response alone does not verify a saved spreadsheet row.

## Verification and next steps

No automated test suite is included. Check required fields, successful submission, failed requests, and stored backend data before using a new deployment. Add inline feedback, submission-state handling, and backend documentation as the next improvements.
