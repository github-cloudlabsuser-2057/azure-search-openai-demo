# Backend Application

This document provides an overview of the backend application.

## Setup

The backend application is built using Quart, a Python framework for asynchronous web applications. The backend code is stored in the `app/backend` folder. The frontend and backend communicate using the AI Chat HTTP Protocol.

### File Processors

The backend application uses file processors to handle different file types. The `setup_file_processors` function in [`prepdocs.py`](app/backend/prepdocs.py) sets up these processors. For example, `.md` files are processed using the `TextParser` and `sentence_text_splitter`.

### Routes

The backend application defines several routes in [`app.py`](app/backend/app.py). Here are a few examples:

- `/`: The index route.
- `/redirect`: An empty page recommended for login redirect to work.
- `/favicon.ico`: Route for the favicon.
- `/assets/<path:path>`: Route for accessing assets.
- `/content/<path>`: Route for accessing content.

## Customization

For more details on customizing the backend, refer to the [customization guide](../../docs/customization.md#customizing-the-backend).

## Deployment

The backend application is deployed using Azure. The deployment configuration is defined in [`infra/main.bicep`](../../infra/main.bicep).