# FKI Business Spend

Public dashboard of every recurring **business** charge at Franchise KI, reconciled from two
independent sources that disagree with each other:

- **Plaid** — real card and bank transactions, via Dash's WORK Subscriptions DB in Notion
- **Billing email** — vendor receipts and past-due notices across `contact@` / `bennett@` / `billing@`

Neither source is complete on its own. A vendor whose card is declining produces **no bank
transaction**, so Plaid cannot see it. A vendor that charges quietly sends **no email**, so the
mail sweep cannot see it. Only the union is the real number.

## Scope

Business lane only. Personal-lane spend is **not** published here, per the Finance HQ standing
rule that personal and business are never mixed. Account digits are last-4 at most, never full numbers.

## Updating

Edit `data/subscriptions.json` and push. The page reads it at load; no build step.

Source of truth for the Plaid side is the Notion WORK Subscriptions DB
(`3e3cf551-4fd3-810a-9650-000b58c88783`), owned by Dash.
