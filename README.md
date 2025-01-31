# micro-frontend-architecture
Micro-Frontend Architecture Using React

Overview

This project demonstrates a Micro-Frontend Architecture using React, where multiple independent applications (Chat App & Email App) are integrated into a Host Application.

Tools & Frameworks Used

React.js – Frontend framework for building UI components.

Webpack Module Federation – For sharing components and state across micro-frontends.

Zustand – A lightweight state management library.

Axios – For API requests (if needed).

Folder Structure

/micro-frontend-app
  /host-app
    /src
      /components
      /store.js  # Zustand store for shared state
      /App.js
    webpack.config.js
  /chat-app
    /src
      /ChatComponent.js
    webpack.config.js
  /email-app
    /src
      /EmailComponent.js
    webpack.config.js

Setup & Running the Application

1. Clone the repository

git clone https://github.com/your-repo/micro-frontend-app.git
cd micro-frontend-app

2. Install Dependencies

cd host-app && npm install
cd ../chat-app && npm install
cd ../email-app && npm install

3. Run Applications

Start the Host App (port 3000):

cd host-app
npm start

Start the Chat App (port 3001):

cd chat-app
npm start

Start the Email App (port 3002):

cd email-app
npm start

Key Architectural Decisions & Trade-Offs

1. Micro-Frontend via Module Federation

Pros:

Independent deployment of Chat & Email apps.

Reusability across projects.

Scalable and modular architecture.

Cons:

Slightly complex setup.

Requires proper state management between apps.

2. Shared State via Zustand

Pros:

Lightweight compared to Redux.

Simple API for managing global state.

Cons:

Not as structured as Redux.

Must ensure proper data updates between micro-frontends.

3. Component Reusability

Shared UI components (buttons, input fields) reside in the Host App for consistency.
