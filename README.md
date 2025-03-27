# Image Annotation Tool

A React-based web application for uploading, viewing, and annotating images with comments and nested replies, inspired by Figma's commenting feature. Built with TypeScript, Zustand for state management, and Tailwind CSS for styling, this tool allows users to collaborate on images by adding comments at specific points, managing threads, and persisting data in localStorage.

This project was developed as part of an assignment for the Frontend Developer role at Officebanao.

## Features

- **Image Upload & Display**:

  - Upload multiple images (JPEG, PNG, etc.) via a simple file input.
  - View images in a responsive gallery grid.
  - Switch between images using a sidebar.

- **Click-to-Comment**:

  - Click anywhere on an image to add a comment.
  - Comments appear as numbered markers at the clicked position.
  - A popup opens at the exact click location for entering comments.

- **Comment Threads & Replies**:

  - Add nested replies to comments, displayed in a thread format.
  - Edit and delete comments and replies directly from the sidebar.

- **State Management**:

  - Uses Zustand for lightweight, centralized state management.
  - Persists images and comments in localStorage for data retention across sessions.

- **Performance Optimization**:
  - Debounced input fields (search, comment, reply) to reduce unnecessary re-renders.
  - Optimized rendering for smooth performance with multiple comments.

## Tech Stack

- **Frontend**: React, TypeScript
- **State Management**: Zustand (with persistence middleware)
- **Styling**: Tailwind CSS
- **Routing**: React Router DOM
- **Notifications**: React Toastify
- **Build Tool**: Vite
- **Deployment**: Vercel (or any hosting platform like Netlify)

## Prerequisites

- Node.js (v16 or higher)
- npm (v7 or higher) or Yarn

## Usage

1. **Upload an Image**:

   - On the homepage or gallery page, click "Upload Image" and select an image file.
   - The image will appear in the gallery and sidebar.

2. **View and Annotate**:

   - Click an image in the gallery to open it in a dialog, or navigate to `/collection` via the sidebar.
   - Click anywhere on the image to add a comment. A popup will appear where you can type your comment.

3. **Manage Comments**:

   - View all comments for the selected image in the sidebar.
   - Click a comment marker to open its thread and add replies.
   - Edit or delete comments/replies directly from the sidebar.

4. **Persistence**:
   - Comments and images are saved in localStorage. Refresh the page to verify persistence.

## Project Structure

```
image-annotation-tool/
├── public/              # Static assets
├── src/
│   ├── components/      # Reusable React components
│   │   ├── CommentPopup.tsx
│   │   ├── CommentsSidebar.tsx
│   │   ├── ImageGallery.tsx
│   │   ├── ImageUpload.tsx
│   │   ├── ImageViewer.tsx
│   ├── store.ts         # Zustand store
│   ├── App.tsx          # Main app component with routing
│   ├── index.css        # Global styles with Tailwind CSS
│   └── main.tsx         # Entry point
├── README.md            # Project documentation
├── package.json         # Dependencies and scripts
└── vite.config.ts       # Vite configuration
```

## Screenshots

- **Gallery View**: Shows uploaded images in a grid.
- **Annotation View**: Displays an image with comment markers and a sidebar.
- **Comment Popup**: Popup for adding comments and replies.

## Future Improvements

- Add user authentication to associate comments with specific users.
- Implement image cropping and drawing tools (currently placeholder buttons).
- Enhance performance with lazy loading for large image sets.
- Add export/import functionality for annotations.

## Assignment Context

This project was built as part of an assignment for the Frontend Developer role at Officebanao. The requirements included building an image annotation tool with image upload, click-to-comment, comment threads, state management, and performance optimization. The UI design is based on the provided Figma prototype.
