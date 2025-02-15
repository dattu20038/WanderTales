# WanderTales

WanderTales is a personal travel journal application that allows users to document their travel experiences, memories, and stories. With features like image uploads, location tagging, date tracking, and favorite marking, WanderTales makes it easy to preserve and revisit your adventures.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [Authentication](#authentication)
  - [Travel Stories](#travel-stories)
  - [Image Uploads](#image-uploads)
  - [Search and Filter](#search-and-filter)
- [Technologies Used](#technologies-used)
- [Contributors](#contributors)


## Features
- **User Authentication**: Secure sign-up and login with JWT-based authentication.
- **Travel Story Management**: Add, edit, delete, and view travel stories.
- **Image Uploads**: Upload images to enrich your travel stories.
- **Search and Filter**: Search stories by title, story, or location, and filter by date range.
- **Favorites**: Mark your favorite travel stories for quick access.
- **Responsive UI**: A clean and modern user interface built with React and Tailwind CSS.

## Installation

### Prerequisites
- Node.js (v16 or higher)
- MongoDB Atlas account (or a local MongoDB instance)
- npm or yarn

### Backend Setup

Clone the repository:

```bash
git clone https://github.com/yourusername/WanderTales.git
cd WanderTales/backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file in the backend directory and add the following environment variables:

```env
ACCESS_TOKEN_SECRET=your_jwt_secret_key
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.xymor.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
```

Start the backend server:

```bash
npm start
```

### Frontend Setup

Navigate to the frontend directory:

```bash
cd ../frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open your browser and navigate to `http://localhost:5173` (or the port specified by Vite).

## Usage

1. **Sign Up / Login**: Create an account or log in using your credentials.
2. **Add a Travel Story**: Click the "Add" button, fill in the details, and upload an image if desired.
3. **View Stories**: Browse through your travel stories on the homepage.
4. **Edit/Delete Stories**: Update or remove existing stories from the view modal.
5. **Search and Filter**: Use the search bar or date picker to find specific stories.

## API Endpoints

### Authentication
- `POST /create-account` : Register a new user.
- `POST /login` : Authenticate and receive a JWT token.

### Travel Stories
- `POST /add-travel-story` : Add a new travel story.
- `GET /get-all-stories` : Retrieve all travel stories for the authenticated user.
- `PUT /edit-story/:id` : Update an existing travel story.
- `DELETE /delete-story/:id` : Delete a travel story.
- `PUT /update-is-favourite/:id` : Toggle the "favorite" status of a story.

### Image Uploads
- `POST /image-upload` : Upload an image.
- `DELETE /delete-image` : Delete an uploaded image.

### Search and Filter
- `GET /search` : Search travel stories by query.
- `GET /travel-stories/filter` : Filter travel stories by date range.

## Technologies Used

### Backend
- Node.js with Express
- MongoDB (via MongoDB Atlas)
- Mongoose for database modeling
- JWT for authentication
- Multer for image uploads
- bcrypt for password hashing

### Frontend
- React with Vite
- Tailwind CSS for styling
- React Router for navigation
- Axios for API calls
- React Toastify for notifications
- React Day Picker for date selection

## Contributing
Contributions are welcome! Feel free to fork the repository, create a feature branch, and submit a pull request.

## Contributors
- **Datta Srivathsava Gollapinni** - [GitHub](https://github.com/dattu20038)
- **N.S.L Karthikeya Reddy** - [GitHub](https://github.com/NSL-Karthikeya-Reddy)

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.
