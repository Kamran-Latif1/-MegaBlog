# MegaBlog

A modern full-stack blog application built with **React** and **Appwrite**. MegaBlog provides authentication, post management, rich-text editing, featured image uploads, and a responsive interface for creating and browsing blog content.

## ✨ Features

- 🔐 **User Authentication**
  - Sign up and log in with Appwrite
  - Protected routes for authenticated users
  - Logout functionality

- 📝 **Blog Post Management**
  - Create new posts
  - Edit existing posts
  - Delete posts
  - View individual posts
  - Browse all available posts

- 🖼️ **Featured Images**
  - Upload featured images for posts
  - Store images in Appwrite Storage
  - Display uploaded images on post cards and individual post pages

- ✍️ **Rich Text Editor**
  - TinyMCE-powered content editor
  - Rich formatting support
  - HTML content rendering

- 🔄 **Automatic Slug Generation**
  - Generates URL-friendly slugs from post titles
  - Updates the slug automatically while editing the title

- 🧭 **Client-Side Routing**
  - React Router-based navigation
  - Protected routes for authenticated functionality

- 🗃️ **State Management**
  - Redux Toolkit
  - Authentication state management with React Redux

- 📱 **Responsive UI**
  - Responsive layouts using Tailwind CSS
  - Reusable UI components

- ⚡ **Modern Development Setup**
  - Vite for development and production builds
  - ESLint for code quality
  - Environment variables for Appwrite configuration

## 🛠️ Tech Stack

### Frontend

- **React 19**
- **React DOM 19**
- **React Router DOM 7**
- **Redux Toolkit**
- **React Redux**
- **React Hook Form**
- **Tailwind CSS**
- **TinyMCE React**
- **HTML React Parser**

### Backend / Services

- **Appwrite**
  - Authentication
  - Database
  - Storage

### Development Tools

- **Vite**
- **ESLint**
- **npm**
- **Git & GitHub**

## 📂 Project Structure

```text
MegaBlog/
├── public/
├── src/
│   ├── Appwrite/
│   │   ├── Auth.js
│   │   └── conf.js
│   │
│   ├── Components/
│   │   ├── Footer/
│   │   ├── Header/
│   │   ├── Postform/
│   │   ├── Button.jsx
│   │   ├── Logo.jsx
│   │   └── index.js
│   │
│   ├── Store/
│   │   ├── Store.js
│   │   └── authSlice.js
│   │
│   ├── pages/
│   │   ├── AddPost.jsx
│   │   ├── AllPost.jsx
│   │   ├── EditPost.jsx
│   │   ├── Home.jsx
│   │   ├── Login.jsx
│   │   ├── Post.jsx
│   │   └── Signup.jsx
│   │
│   ├── App.jsx
│   ├── AuthLayout.jsx
│   ├── Login.jsx
│   ├── PostCard.jsx
│   ├── RTE.jsx
│   ├── Signup.jsx
│   ├── input.jsx
│   ├── select.jsx
│   └── main.jsx
│
├── .env.example
├── .gitignore
├── eslint.config.js
├── package.json
├── tailwind.config.js
├── vite.config.js
└── README.md
```

## 🚀 Getting Started

### Prerequisites

Make sure you have installed:

- [Node.js](https://nodejs.org/)
- npm
- An Appwrite project

### 1. Clone the repository

```bash
git clone https://github.com/Kamran-Latif1/-MegaBlog.git
cd MegaBlog
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env` file in the project root.

You can use `.env.example` as the template:

```bash
cp .env.example .env
```

On Windows PowerShell, you can also create the file manually.

Add your Appwrite configuration:

```env
VITE_APPWRITE_URL=
VITE_APPWRITE_PROJECT_ID=
VITE_APPWRITE_DATABASE_ID=
VITE_APPWRITE_COLLECTION_ID=
VITE_APPWRITE_BUCKET_ID=
```

Fill each variable with the corresponding value from your Appwrite project.

> **Important:** Never commit your real `.env` file to GitHub. The project already ignores `.env` through `.gitignore`.

### 4. Configure Appwrite

Create/configure an Appwrite project with:

- An **Authentication** service for user accounts
- A **Database** for blog posts
- An **Images/Storage bucket** for featured images
- Appropriate read/write permissions for your application

The database should contain the attributes required by the application, including:

- `title`
- `content`
- `featuredImage`
- `status`
- `userId`

## ▶️ Run the Development Server

Start the Vite development server:

```bash
npm run dev
```

Vite will provide a local development URL, typically:

```text
http://localhost:5173
```

## 🧪 Code Quality

Run ESLint:

```bash
npm run lint
```

The project currently has no ESLint errors. React Hook Form's `watch()` API may produce a React Compiler compatibility warning; this does not prevent the application from running or building successfully.

## 🏗️ Production Build

Create a production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

## 🔒 Environment Variables

| Variable                      | Purpose                               |
| ----------------------------- | ------------------------------------- |
| `VITE_APPWRITE_URL`           | Appwrite API endpoint                 |
| `VITE_APPWRITE_PROJECT_ID`    | Appwrite project ID                   |
| `VITE_APPWRITE_DATABASE_ID`   | Appwrite database ID                  |
| `VITE_APPWRITE_COLLECTION_ID` | Blog posts collection/table ID        |
| `VITE_APPWRITE_BUCKET_ID`     | Storage bucket ID for featured images |

## 🔄 Application Flow

```text
User
  │
  ├── Sign Up / Login
  │        │
  │        ▼
  │    Appwrite Auth
  │        │
  │        ▼
  │   Redux Auth State
  │
  └── Authenticated User
           │
           ├── Create Post
           ├── Edit Post
           ├── Delete Post
           ├── Upload Image
           └── View Posts
                    │
                    ▼
              Appwrite Database
                    +
              Appwrite Storage
```

## 📌 Key Concepts Demonstrated

This project demonstrates practical use of:

- React component architecture
- React Hooks
- React Router
- Protected routes
- Redux Toolkit state management
- Appwrite authentication
- Appwrite database operations
- Appwrite file storage
- React Hook Form
- Rich-text editing
- Reusable components
- Environment-based configuration
- CRUD operations
- Git and GitHub workflow

## 📦 Main Dependencies

The project uses the following major packages:

```text
React                 19.2.8
React DOM             19.2.8
Vite                  8.2.1
Appwrite              26.2.0
React Router DOM      7.18.2
Redux Toolkit         2.12.0
React Redux           9.3.0
React Hook Form       7.85.0
TinyMCE React         6.3.0
HTML React Parser     6.1.7
Tailwind CSS          3.4.19
```

## 👨‍💻 Author

**Kamran Latif**

GitHub: [Kamran-Latif1](https://github.com/Kamran-Latif1)

## 📄 License

This project currently does not include a license.

---

### Development Note

MegaBlog was built as a practical React project to apply concepts including authentication, state management, routing, forms, CRUD operations, API integration, file storage, and reusable component design.
