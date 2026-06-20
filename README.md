# AI Food Recipe Generator

Upload a photo of your ingredients or a dish, and AI generates personalized recipes with nutritional information.

## Features

- **Image Analysis** — Upload a food photo; AI detects ingredients automatically
- **AI Recipe Generation** — Generates detailed recipes with ingredients, step-by-step instructions, and nutrition breakdown
- **Recipe Suggestions** — Get multiple recipe ideas based on available ingredients
- **Dietary Preferences** — Filter results by vegan, keto, gluten-free, high-protein, and more
- **Save & Manage** — Save recipes and browse/search/filter them later

## Tech Stack

**Client:** React 18, React Router, Vite, Axios  
**Server:** Node.js, Express, MongoDB (Mongoose), Multer  
**AI:** Groq SDK (LLaMA 4 Scout for vision, LLaMA 3.3 70B for text)

## Getting Started

### Prerequisites

- Node.js 18+
- MongoDB (local or Atlas)
- Groq API key — get one at [console.groq.com](https://console.groq.com)

### 1. Clone and install

```bash
git clone https://github.com/manoj-kumar-43/ai_food_recipe.git
cd ai_food_recipe
```

**Server:**
```bash
cd server
npm install
```

**Client:**
```bash
cd client
npm install
```

### 2. Configure environment

Copy the example env file and add your Groq API key:

```bash
cp server/.env.example server/.env
```

Edit `server/.env`:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/ai-recipe-generator
GROQ_API_KEY=your_groq_api_key_here
```

### 3. Run

Start both server and client:

```bash
# Terminal 1 — Server
cd server
npm run dev

# Terminal 2 — Client
cd client
npm run dev
```

Open `http://localhost:5173` in your browser.

### 4. Build for production

```bash
cd client
npm run build
```

## API Endpoints

| Method | Endpoint               | Description              |
| ------ | ---------------------- | ------------------------ |
| POST   | `/api/recipes/analyze` | Upload image for analysis |
| POST   | `/api/recipes/generate`| Generate a recipe         |
| POST   | `/api/recipes/suggestions` | Get recipe suggestions |
| POST   | `/api/recipes/save`    | Save a recipe             |
| GET    | `/api/recipes/saved`   | Get all saved recipes     |
| GET    | `/api/recipes/saved/:id` | Get a single recipe     |
| DELETE | `/api/recipes/saved/:id` | Delete a recipe         |
| GET    | `/api/health`          | Health check              |

## 🎥 Project Demo

<a href="https://res.cloudinary.com/dbbxkwmcu/video/upload/v1781938498/VID_20260612_195544_ro2zlb.mp4">
  <img src="./assets/demo-thumbnail.png" alt="Project Demo" width="800">
</a>

## 🎥 Demo Video

[▶️ Watch Demo Video](https://res.cloudinary.com/dbbxkwmcu/video/upload/v1781938498/VID_20260612_195544_ro2zlb.mp4)
