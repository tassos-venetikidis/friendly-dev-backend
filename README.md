# Friendly Dev Strapi Backend

This is the **Strapi backend** for the **Friendly Dev** website. It provides the API for managing **projects** and **blog posts** displayed on the frontend.

You can find the frontend React website [here](https://github.com/tassos-venetikidis/friendly-dev-frontend).

---

## 🧱 Features

- REST API for Projects and Blog Posts
- Rich media upload support (via Strapi Media Library)
- Cloudinary integration for image uploads
- Custom fields including image, tags, description, etc.
- Role-based admin panel
- Easily deployable to services like Render, Railway, or DigitalOcean

---

## 🛠️ Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/tassos-venetikidis/friendly-dev-backend.git
cd friendly-dev-backend
```

2. Install Dependencies

```bash
npm install
```

3. Configure Environment

Copy the example env file:

```bash
cp .env.example .env
```

Then update .env with your database connection and other required settings. We use a Neon PostgreSQL database. So you need to create an account at neon.com and then add your own database string.

4. Start the Server

```bash
npm run develop
```

This will launch Strapi in development mode at:

```
http://localhost:1337/admin
```

📦 API Endpoints

Example public endpoints:

- /api/posts
- /api/projects

You can use query parameters for:

- Sorting: ?sort=date:desc
- Filtering: ?filters[category][$eq]=design
- Pagination: ?pagination[limit]=5
- Population: ?populate=image

🔐 Permissions

Make sure to allow public access to the required content types:

- Go to `Settings > Roles > Public`

- Enable `find` and `findOne` for post and project

🖼 Media Uploads

By default, media is stored locally under `/public/uploads`.

This project uses Cloudinary. You need to add the keys from your own Cloudinary account.

Tassos Venetikidis, March 2026.
