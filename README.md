# AluraBooks

A bookstore front-end in plain HTML, CSS and JavaScript: a landing page with carousels of releases and best sellers, plus a "Minha estante" page that loads a book catalog from an API and lets you filter, sort and total it.

**Live demo:** [alurabooks-rose-zeta.vercel.app](https://alurabooks-rose-zeta.vercel.app)

## What's inside

The shelf page (`pages/minha-estante.html`) is where the JavaScript is. Each file in `app/` covers one array method:

| File | What it does |
|---|---|
| `main.js` | Fetches the book list from a public JSON endpoint with `fetch` and `async/await` |
| `metodoMap.js` | `map` applies a 30% discount to every price |
| `metodoForEach.js` | `forEach` renders each book as a card, and greys out the ones with no stock |
| `metodoFilter.js` | `filter` powers the category buttons (front-end, back-end, data) and the "available" button |
| `metodoReduce.js` | `reduce` adds up the price of the available books and shows the total |
| `metodoSort.js` | `sort` orders the books by price |

The landing page uses the Swiper library for its carousels. The CSS is split into one file per section (header, banner, carousel, topics, contact, footer, shelf), with media queries for smaller screens.

The interface is in Portuguese.

## Run it

No build step and no dependencies to install. The shelf page fetches data over the network, so run it from a local server and not from a `file://` address:

```bash
git clone https://github.com/victorhubarb/alurabooks.git
cd alurabooks
python3 -m http.server 8000     # then open http://localhost:8000
```

## Project structure

```
index.html            Landing page
pages/                minha-estante.html
app/                  JavaScript, one file per array method
styles/ + styles.css  CSS by section
img/                  Covers, banners and icons
```

## Known gaps

- After you click a filter button, prices show without the discount. The discounted list is not saved back into `livros`, and the filters read the original array.
- "Ordenar por preço" sorts the original array in place and also clears any active filter.
- Search, a shopping cart and checkout are not part of this project. It only covers browsing and filtering.
- The catalog comes from a third-party endpoint, so the page depends on it staying online.
- The shelf page has no loading or error state.

---

Victor Hugo Barbosa · [GitHub](https://github.com/victorhubarb) · [LinkedIn](https://www.linkedin.com/in/victorhbarbosa/)
