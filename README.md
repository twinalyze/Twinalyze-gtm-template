# Twinalyze Web Analytics GTM Template

Twinalyze Web Analytics is a Google Tag Manager custom template for installing the Twinalyze Web SDK, enabling automatic website event tracking, and sending custom events from Google Tag Manager.

## Features

- Initialize Twinalyze Web SDK through Google Tag Manager
- Track automatic events:
  - pageView
  - scrollDepth
  - elementClick
  - formStart
  - formSubmit
  - searchResultsView
  - fileDownload
- Send custom events using GTM triggers and variables
- Supports configurable API base URL, SDK URL, SDK version, and debug mode

## Setup

1. Add the template to your Google Tag Manager workspace.
2. Create a new Twinalyze Web Analytics tag.
3. Select **Initialize SDK**.
4. Enter your Twinalyze API Key.
5. Enter your Twinalyze Client Token / Public Write Key.
6. Set the trigger to **Initialization - All Pages**.
7. Save and publish your GTM container.

## Custom Events

To send a custom event, push data to the GTM dataLayer:

```js
window.dataLayer = window.dataLayer || [];
window.dataLayer.push({
  event: "add_to_cart",
  product_id: "P123",
  product_name: "Pearl Hair Clip",
  price: 499,
  currency: "INR"
});