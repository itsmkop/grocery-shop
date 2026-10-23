# Apni Dukaan — Grocery Shop

Ek hi code se **teen apps** — company, retailer aur grahak.

| Role | Kaun | URL | Android app |
|---|---|---|---|
| **Company** | owner / distributor | https://itsmkop.github.io/grocery-shop/company/ | Apni Dukaan Company |
| **Retailer** | dukaan malik | https://itsmkop.github.io/grocery-shop/retailer/ | Apni Dukaan Retailer |
| **Public** | grahak | https://itsmkop.github.io/grocery-shop/ | Apni Dukaan |

Sab data ek hi file me: `data.json`

## Company app
- Default PIN: `1234`
- Retailer **add / edit / remove / block-unblock**
- **Make public** — kaunsi dukaan public app me live dikhegi
- Shop info, products, GitHub cloud sync

## Retailer app
- Login: **code + PIN** (company deta hai)
- Apne products add / edit / delete
- Sirf apne products dikhte hain — dusre retailer ka na dikhta hai na edit hota hai
- Company block kare to Blocked screen

## Public app
- Grahak ke liye Flipkart-style shop
- Company ke chune hue retailer ki dukaan + uske products
- Search, cart, WhatsApp / UPI order, my orders

## Cloud sync
- Company aur Retailer app ke Cloud tab me ek baar GitHub token daalo
- Uske baad har save apne-aap online chala jata hai
- Token sirf us phone / browser me rehta hai

## Android apps
- Teen alag APK, alag package — ek hi project se (product flavors)
- APK me **kuch bhi bundled nahi** — har app seedha website se load karta hai
- Isliye: **website update = app update** (rebuild ki zaroorat nahi)
- App kholne ke liye internet zaroori hai (pehli baar)

## Repo layout
```
index.html            public app
retailer/index.html   retailer app
company/index.html    company app
data.json             sabka data (retailers + products)
```
GitHub Pages: Settings → Pages → Branch `main`, Folder `/ (root)`

Purana `admin.html` ab company app ka kaam karta hai — uski zaroorat nahi.

## Note
- Token sirf browser / phone me hi rehta hai
- `data.json` public URL se padha ja sakta hai, aur block client-side hai — pakki security ke liye backend chahiye
