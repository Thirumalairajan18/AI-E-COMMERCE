# AI E-Commerce Customer Support Agent — VS Code Test Version

This version is designed to run locally in VS Code with **no API key and no installation**.

## Run

1. Extract/open this folder in VS Code.
2. Open `app/index.html` in a browser.
3. For the best development experience, install the VS Code **Live Server** extension and choose **Open with Live Server**.

## Test these messages

- `Where is my order ORD-48210?`
- `I want to return my order ORD-30056, the item doesn't fit.`
- `I need a lightweight laptop bag under ₹2000 for my daily commute.`
- `Tell me about the FeatherLite Sling Laptop Bag.`
- `My name is Rajan`
- `Where is my order ORD-48210?` (tests memory/order context)

## What this local version demonstrates

Customer Query → Intent Understanding → Memory Check → Tool Selection → Tool Execution → Response Generation

Implemented local tools:
- `get_order_status`
- `initiate_return`
- `recommend_products`
- `get_product_info`
- `save_customer_memory`
- `get_customer_memory`

Order and product information are mock data, matching the project report/use-case. Browser `localStorage` is used for memory.

## Important

The original GitHub project calls the Anthropic API directly from the browser and relies on `window.storage`, which are not standard for a normal VS Code/browser setup. This test version replaces those dependencies with local implementations so you can immediately demonstrate the project flow.

For a production/real-AI version, the API key should be kept on a backend server rather than placed in browser JavaScript.
