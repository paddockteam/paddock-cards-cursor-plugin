# Paddock Cards for Cursor

Send birthday cards, Christmas cards, thank-you cards, sympathy cards, congratulations cards and postcards. Paddock prints and mails them for you. No Paddock account is needed; you sign in to Stripe Link once and approve every purchase yourself.

## Install

Add the server in `~/.cursor/mcp.json` or `.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "paddock-cards": {
      "url": "https://api.paddock.so/agent-commerce/mcp/connected"
    }
  }
}
```

Cursor asks you to sign in the first time. The sign-in connects your Stripe Link account to this server; Link is available to customers in the United States and Canada.

To browse and order without signing in, use the public server instead. It offers the same tools; `pay_order` then connects Link for one order at a time, and order history is unavailable.

```json
{
  "mcpServers": {
    "paddock-cards": {
      "url": "https://api.paddock.so/agent-commerce/mcp"
    }
  }
}
```

## Try

- Send a funny birthday card to my brother in Denver
- Find a calm sympathy card with no words on the front
- Mail three thank-you postcards to my team for Friday

## What the agent can do

Search the catalog by occasion, mood, format, artist or budget. Prepare one card or up to five hundred in a single order, each with its own design, message, recipient and mailing date. Show the finished card before you decide. Change an unpaid draft. Add your own photo, logo or QR code through a private upload page that you open yourself. Pay with your Link approval, or hand you a review link to pay by card. Check printing and mailing progress and cancel eligible cards. With order-history permission, list the orders made through this connection.

Prices are read live for each card's destination and include postage and applicable tax. Preparing an order never charges you. Nothing is paid until you approve the exact purchase in Link or pay on the review page. Cursor asks before running a tool unless you allow it.

## Permissions

Paddock supports these permissions. The consent screen shows which ones Cursor requests:

- `wallet:pay` lets Paddock request your approval in Link for each exact purchase and complete it after you approve.
- `orders:read` lets this connection list and read the orders it creates from now on, including card contents and addresses. Earlier orders and other connections are not included. A payment-only connection cannot list orders.

Paddock keeps your Link credentials encrypted on its server. The agent never receives your Link credentials or card details. Disconnect Paddock in Link to revoke wallet access. Removing this server alone does not revoke the saved Link connection. Saved connections expire after one year at most.

## Configuration

None. The plugin declares no variables and needs no keys.

## Privacy and terms

Recipient names and mailing addresses are used to print and mail the card.

Privacy: https://paddock.so/privacy/ · Terms: https://api.paddock.so/agent-commerce/terms · Support: https://paddock.so/support/ or team@paddock.so · Guide: https://paddock.so/agent-commerce/guide/

## License

This repository holds configuration and documentation only, under the MIT License. Paddock Technologies Inc., Santa Fe, New Mexico.
