Streamify - A Lightweight Twitch-Style CloneStreamify is a high-performance, front-end-only Twitch-style clone built with vanilla HTML, CSS, and JavaScript. This project serves as a demonstration of core web development proficiency and modern front-end architecture without relying on heavy frameworks.✨ Features🎨 Responsive Design: A mobile-first layout that adapts seamlessly to all screen sizes.🌗 Dark/Light Theme: Supports system color scheme preference and allows manual toggling, with the user's choice saved in localStorage.🔍 Client-Side Search: A debounced search input to instantly filter streams by title, channel, or category.▶️ HLS Video Playback: Utilizes the standard <video> element with hls.js as a fallback for broad browser compatibility.❤️ Follow System: "Follow" and "unfollow" channels, with the state persisted in the browser's localStorage.💬 Live Chat: Features a mock mode for demo purposes and an optional real-time mode via WebSockets.♿ Accessibility: Built with semantic HTML, ARIA attributes, and keyboard navigation in mind.🚀 How to RunYou can run this project in two modes: Mock Mode (front-end only) or Realtime Mode (with a WebSocket server for chat).Mode 1: Mock Mode (No Server Needed)This is the easiest way to see the front-end in action. The chat will be simulated.Clone the repository:git clone [https://github.com/your-username/streamify.git](https://github.com/your-username/streamify.git)
cd streamify
Open index.html in your browser.You can open the file directly from your file system. However, if you encounter a CORS error with the video player, it's recommended to run a simple local server:npx serve
Mode 2: Realtime Chat ModeThis mode enables the live chat feature by running a small Node.js WebSocket server.Prerequisites:You must have Node.js installed on your machine.Install dependencies:This will install the ws library required for the WebSocket server.npm install ws
Start the WebSocket server:node server.js
Update the chat mode:In the modules/chat.js file, change the CHAT_MODE constant from 'mock' to 'websocket'.Run the front-end:Open index.html using a local server as described in Mock Mode.npx serve
🏗️ Architecture & DesignThe project adheres to several core principles to ensure a clean, maintainable, and lightweight codebase.Vanilla First: No frameworks (like React, Vue, or Angular) were used. This focuses on core web technologies and performance.Modular JavaScript: The code is organized into ES6 modules to promote separation of concerns (e.g., API logic, DOM manipulation, state management).Simple State Management: Global state is managed in simple JavaScript objects, sufficient for the project's scope.Data-Driven UI: The user interface is rendered dynamically from a mock data.json file, simulating a real API and making content changes easy.Modern CSS: A comprehensive set of CSS variables (design tokens) are used for easy theming and a consistent design system.Project Structure/
├── 📂 assets/              # Placeholder images, logos, etc.
├── 📂 modules/             # Self-contained JavaScript modules
│   ├── 📜 api.js           # Handles data fetching
│   ├── 📜 chat.js          # Logic for mock & WebSocket chat
│   ├── 📜 dom.js           # DOM manipulation helpers
│   ├── 📜 storage.js       # localStorage interaction
│   └── 📜 ...              # Other helper modules
├── 📜 index.html           # Homepage for stream discovery
├── 📜 channel.html         # Single channel/video page
├── 📜 data.json            # Mock data for channels and categories
└── 📜 server.js (Optional) # Minimal Node.js WebSocket server
⚠️ LimitationsNo Backend/Database: All data is pulled from a static data.json file. State (like followed channels) is stored only in the user's browser.No Authentication: There is no user login or authentication system.Mock VODs: The video player uses a single sample video file for all streams for demonstration purposes.📄 LicenseThis project is licensed under the MIT License. See the LICENSE file for details.

---

## 👨‍💻 Built by Girish Lade

**Streamify** is an open-source project by [Girish Lade](https://github.com/girishlade111).

Check out more projects at [ladestack.in](https://ladestack.in).
