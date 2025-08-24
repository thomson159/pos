# POS Fullstack App – Backend + Frontend Integration

This repository connects two separate projects:

- **Backend (Express + MongoDB + REST API)**: [pos-backend](https://github.com/thomson159/pos-backend)  
  Production API Docs: [https://pos-backend-kso1.onrender.com/api-docs/](https://pos-backend-kso1.onrender.com/api-docs/)
  
- **Frontend (React)**: [pen](https://github.com/thomson159/pen)  
  Production frontend (only `/shop` is relevant): [https://243pen.store/shop](https://243pen.store/shop)

---

## 📦 Backend

A complete REST API for managing products, orders, and syncing with external sources.

Repo: [pos-backend](https://github.com/thomson159/pos-backend)  
Docs: [API Swagger](https://pos-backend-kso1.onrender.com/api-docs/)

### 📌 Issues and TODOs

- ❌ **Unit tests for `/orders`** only work with a live DB – mock-based tests currently have issues.
- ❌ **On production**, endpoints `/products/remote` and `/products/sync` are not working correctly – possibly a config/hosting issue on [Render](https://render.com/).
- ❌ **Type check**:
  - `total` is currently a string (`"total": "1.00"`), should likely be a `number`.
  - `price` and `product_price` are correct as floats (`10.0`, `10.99`).

```bash
git clone https://github.com/thomson159/pos-backend
cd pos-backend
npm install
npm run dev
```

---

## 🛒 Frontend

Repo: [pen](https://github.com/thomson159/pen)  
Live: [https://243pen.store/shop](https://243pen.store/shop)

### Note:
- Only the `/shop` page is connected to the backend.
- Other parts of the frontend project are not relevant to this integration.


```bash
git clone https://github.com/thomson159/pen
cd pen
npm install
npm start
```

## Notes

Backend has detailed Swagger documentation.

Frontend is partially connected – only /shop integrates with the API.

The project is fully functional locally; production may need some fine-tuning on the backend side (especially sync endpoints).
