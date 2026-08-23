# Buying Shortlist Skill

## Name
buying-shortlist-telegram

## Purpose
Create a current, practical buying shortlist for the user, optimized for Telegram sharing.

## Trigger
Use this skill when the user asks to:
- find products to buy
- compare products
- give a top 3 / top 5 / top 10 shortlist
- recommend a laptop, phone, PC part, appliance, or other purchasable product
- re-check current price, stock, store, phone, or map

## Required behavior
1. Verify current product listings when the information can change.
2. Respect the user's budget and minimum requirements exactly.
3. Rank options by the user's stated use case, not only raw specs.
4. Prefer direct product pages over category/search pages.
5. Include store contact details and Google Maps links when available.
6. Flag stale, inconsistent, or suspicious listings.
7. Do not rank an item highly only because its model name sounds newer.
8. Keep the final answer easy to paste into Telegram.

## Telegram output format

💻 **Top {N} {Product Type} Under ${Budget} for {Use Case}**

🥇 **1. {Product Name}**
• CPU/Chip: {CPU or main processor}
• RAM: {RAM}
• Storage: {Storage}
• Screen / Key Spec: {Display or important spec}
• Price: **${Price}**
🔗 [Product]({Direct Product URL})
📞 {Shop Name}: {Phone if available}
📍 [Google Maps]({Google Maps URL if available})

==============

🥈 **2. {Product Name}**
• CPU/Chip: {CPU or main processor}
• RAM: {RAM}
• Storage: {Storage}
• Screen / Key Spec: {Display or important spec}
• Price: **${Price}**
🔗 [Product]({Direct Product URL})
📞 {Shop Name}: {Phone if available}
📍 [Google Maps]({Google Maps URL if available})

==============

Continue the same structure for all ranked products.

At the end:

==============
✅ **Best Overall:** {Product} — ${Price}
💰 **Best Value:** {Product} — ${Price}
🎯 **Best for {Use Case}:** {Product}

## Ranking guidance for laptops
For IT students, prioritize:
1. 16GB RAM minimum
2. CPU performance for coding, Docker, VMs, Android Studio, databases, and multitasking
3. 512GB SSD minimum
4. Good 16:10 or IPS/OLED display
5. RAM/SSD upgradeability
6. Battery life and portability
7. Warranty and brand/service quality
8. Price/value

Do not overvalue weak CPUs with newer-looking names. For example, compare actual core/thread count, architecture, and benchmark class.

## Link rules
- Product link: direct retailer product page whenever possible.
- Map link: Google Maps search or exact location link.
- Phone: use verified store/business phone if available.
- If map or phone is unavailable, omit that line rather than guessing.

## Separator
Always use exactly:

==============

between products.

## Style
- Telegram-friendly
- concise
- emoji allowed
- no markdown tables unless the user specifically asks for a table
- keep recommendations practical and decisive
