# Introduction
This [node.js](https://nodejs.org/) demo application illustrates how to fetch completed call events for our GoTo Connect product.

It does so by creating a Call Events Reports notification subscription that receives a notification after each call completes. This notification contains a call identifier that is then used to fetch the matching call events through a REST API.

This demo is meant to be used along with our [Call Events Report](https://developer.goto.com/guides/GoToConnect/16_CallEventsReport/) developer guide.


## How to run this demo

### Prerequisites

#### OAuth Client

You will need an OAuth client for the app (refer to the [OAuth Clients documentation](https://developer.goto.com/guides/Authentication/04_HOW_accessTokenNodeJS/) to create one) with a redirect URI set to: `http://127.0.0.1:12021/app/redirect`

#### Environment variables

You will need to create a `.env` configuration file with the following content:

```
OAUTH_CLIENT_ID=<your_client_id>
OAUTH_CLIENT_SECRET=<your_client_secret>
ACCOUNT_KEY=<your_acount_key>
LOG_LEVEL=info # or debug
```

### Running the app

The app can then be started by running:

* `npm install` (only once)
* `node app` or `npm start`
