**Admin Login:**
- **Email:** kanikapunia119@gmail.com
- **Password:** kanika1106

# Quickblog

Quickblog is a full-stack blogging platform built with the MERN stack (MongoDB, Express.js, React.js, Node.js). It provides a simple and intuitive interface for creating, managing, and reading blog posts. The application also includes an admin panel for managing blogs and comments, and a feature to generate blog content using a generative AI model.

## Features

- **Create, Read, Update, and Delete (CRUD) operations for blog posts.**
- **User-friendly rich text editor for writing blog posts.**
- **Admin panel for managing all blogs and comments.**
- **Approve or delete comments.**
- **Publish or unpublish blogs.**
- **Generate blog content using a generative AI model.**
- **Responsive design for a seamless experience on all devices.**

## Tech Stack

### Frontend

- **React.js:** A JavaScript library for building user interfaces.
- **Vite:** A fast build tool for modern web development.
- **React Router:** For handling client-side routing.
- **Axios:** For making HTTP requests to the backend.
- **Tailwind CSS:** A utility-first CSS framework for styling.
- **Quill:** A powerful rich text editor.

### Backend

- **Node.js:** A JavaScript runtime for building server-side applications.
- **Express.js:** A web application framework for Node.js.
- **MongoDB:** A NoSQL database for storing data.
- **Mongoose:** An ODM (Object Data Modeling) library for MongoDB.
- **JSON Web Tokens (JWT):** For user authentication and authorization.
- **ImageKit:** For image storage and optimization.
- **Google Generative AI:** For generating blog content.

## File Structure

```
Quickblog/
├── client/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── package.json
│   └── vite.config.js
├── server/
│   ├── configs/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── package.json
│   └── server.js
├── .gitignore
├── package.json
└── README.md
```

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

- **Node.js and npm:** Make sure you have Node.js and npm installed on your machine. You can download them from [here](https://nodejs.org/).
- **MongoDB:** You need to have a MongoDB database. You can use a local MongoDB instance or a cloud-based service like MongoDB Atlas.

### Installation

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/KanikaPunia119/BlogNest.git
    ```

2.  **Navigate to the project directory:**

    ```sh
    cd BlogNest
    ```

3.  **Install server dependencies:**

    ```sh
    cd server
    npm install
    ```

4.  **Install client dependencies:**

    ```sh
    cd ../client
    npm install
    ```

5.  **Create a `.env` file in the `server` directory and add the following environment variables:**

    ```
    PORT=3000
    MONGO_URI=<your_mongodb_uri>
    JWT_SECRET=<your_jwt_secret>
    IMAGEKIT_PUBLIC_KEY=<your_imagekit_public_key>
    IMAGEKIT_PRIVATE_KEY=<your_imagekit_private_key>
    IMAGEKIT_URL_ENDPOINT=<your_imagekit_url_endpoint>
    GEMINI_API_KEY=<your_gemini_api_key>
    ```

### Usage

1.  **Start the server:**

    ```sh
    cd server
    npm run server
    ```

2.  **Start the client:**

    ```sh
    cd ../client
    npm run dev
    ```

The application will be running at `http://localhost:5173`.

## API Endpoints

### Admin Routes

-   `POST /api/admin/login`: Login as an admin.
-   `GET /api/admin/comments`: Get all comments (admin only).
-   `GET /api/admin/blogs`: Get all blogs (admin only).
-   `POST /api/admin/delete-comment`: Delete a comment by ID (admin only).
-   `POST /api/admin/approve-comment`: Approve a comment by ID (admin only).
-   `GET /api/admin/dashboard`: Get dashboard stats (admin only).

### Blog Routes

-   `POST /api/blog/add`: Add a new blog post (admin only).
-   `GET /api/blog/all`: Get all published blog posts.
-   `GET /api/blog/:blogId`: Get a single blog post by ID.
-   `POST /api/blog/delete`: Delete a blog post by ID (admin only).
-   `POST /api/blog/toggle-publish`: Toggle the publish status of a blog post (admin only).
-   `POST /api/blog/add-comment`: Add a comment to a blog post.
-   `POST /api/blog/comments`: Get all approved comments for a blog post.
-   `POST /api/blog/generate`: Generate blog content using AI (admin only).


## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request