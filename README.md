# QUIET BATTLES™ – Frontend Client

> *"WEAR YOUR BATTLES."*  
> High-concept architectural luxury streetwear e-commerce & editorial storytelling client application for **QUIET BATTLES™**.

---

## 1. Technology Stack

- **Framework**: React 18 (Vite SPA)
- **Language**: JavaScript (Zero TypeScript)
- **Styling**: Tailwind CSS with custom editorial typography
- **State Management**: React Context API (`AdminContext`, `ContentContext`, `CartContext`)
- **Routing**: React Router DOM v6
- **Animations**: Framer Motion
- **HTTP Client**: Axios with automated JWT Bearer interceptors
- **Icons**: Lucide React
- **Hosting / Deployment**: Vercel (`vercel.json`)

---

## 2. Project Structure

```
quiet-battles-frontend/
├── public/                 # Static brand assets
├── src/
│   ├── components/         # Modular reusable UI components
│   │   ├── admin/          # CMS data tables, forms, badges
│   │   ├── archive/        # Editorial story sections, chapter grids
│   │   ├── common/         # EditorialImage, ErrorBoundary, PageTransition
│   │   ├── home/           # Hero, brand philosophy, featured garments
│   │   ├── layout/         # Navbar, Footer
│   │   └── product/        # ProductCard, ProductGallery, SizeSelector
│   ├── context/            # AdminContext, ContentContext, CartContext
│   ├── data/               # High-fidelity fallback archival datasets
│   ├── hooks/              # Custom React hooks (useDocumentTitle)
│   ├── layouts/            # PublicLayout, AdminLayout
│   ├── pages/              # Home, Archive, SeriesDetail, ChapterDetail, Shop, ProductDetail, Cart
│   │   └── admin/          # AdminLogin, AdminDashboard, Series, Chapter, Product Management
│   ├── routes/             # AppRoutes, ProtectedRoute
│   ├── services/           # api.js, authService, seriesService, chapterService, productService, productImageService
│   └── utils/              # slugify, formatCurrency, constants
├── index.html              # HTML5 entry template
├── package.json
├── tailwind.config.js
├── vercel.json             # Vercel SPA routing rewrites
├── vite.config.js
└── .env.example
```

---

## 3. Local Development Setup

### Prerequisites
- Node.js 18+ and npm (`node -v`)

### Installation & Run
```bash
# 1. Install dependencies
npm install

# 2. Configure environment
cp .env.example .env

# 3. Start development server
npm run dev
```

The application will start on: **`http://localhost:3000`**

### Production Build
```bash
npm run build
npm run preview
```

---

## 4. Environment Variables

| Variable | Description | Default |
|---|---|---|
| `VITE_API_BASE_URL` | Base URL for Spring Boot REST API | `http://localhost:8081/api/v1` |

---

## 5. Deployment Guide (Vercel)

1. Push this repository to GitHub.
2. In Vercel, select **Add New** $\rightarrow$ **Project** $\rightarrow$ Import this repository.
3. Configuration settings:
   - **Framework Preset**: Vite
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
4. Set Environment Variable:
   - `VITE_API_BASE_URL`: `https://<your-backend-host>/api/v1`
5. Click **Deploy**. Vercel will deploy the client with clean SPA rewrites configured in `vercel.json`.

