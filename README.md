# Myntra Clone: Frontend

A React + Redux Toolkit clone of the **Myntra** fashion e-commerce storefront. It loads a product catalogue from an Express API, shows it in a responsive grid, and lets you add and remove items in a shopping bag that shows a live price summary.

**Backend repo:** [Myntra-backend](https://github.com/mayurgarg08/Myntra-backend)

## Features

- Myntra-style header with category navigation, search bar and bag counter
- Product grid with image, brand, name, current and original price, discount and rating
- **Add to / remove from bag**, with state managed in Redux Toolkit
- **Bag page** with item cards (return period, delivery date) and a price summary (total MRP, discount, convenience fee, final amount)
- A loading spinner while products are fetched. Requests use `AbortController` so they are cancelled cleanly.
- Fetch status tracked in Redux so the catalogue is only loaded once

## Tech stack

React 19 · Vite · Redux Toolkit · React Redux · React Router · Bootstrap · React Icons

## Project structure

```
src/
  routes/
    App.jsx           layout: Header, <Outlet/>, Footer, loading state
    Home.jsx          product grid
  components/
    Header.jsx, Footer.jsx
    HomeItem.jsx      product card
    Bag.jsx, BagItem.jsx, BagSummary.jsx
    FetchItems.jsx    loads items from the API into Redux
    Loading.jsx
  store/
    index.js          configureStore
    itemSlice.js      product list
    bagSlice.js       bag item IDs
    fetchStatusSlice.js
public/images/        product images
```

## Getting started

### Prerequisites
- Node.js 18+
- The [Myntra backend](https://github.com/mayurgarg08/Myntra-backend) running on `http://localhost:8080`

```bash
git clone https://github.com/mayurgarg08/Myntra-frontend.git
cd Myntra-frontend
npm install
npm run dev       # http://localhost:5173
```

| Route | Page |
| --- | --- |
| `/` | Home: product catalogue |
| `/Bag` | Shopping bag and price summary |

### Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the dev server |
| `npm run build` | Production build |
| `npm run preview` | Preview the build |
| `npm run lint` | Run ESLint |

## Author

**Mayur Garg** · [GitHub](https://github.com/mayurgarg08) · [LinkedIn](https://www.linkedin.com/in/mayur-garg-428a291b4/)
