# TrendSpark Bharat

AI-powered content pack generator for Indian micro-creators. Generate culturally relevant captions, hashtags, post ideas, reel scripts, and trending topic styles across 8 Indian languages.

## Features

- 🌐 **Multi-language Support**: Hindi, Hinglish, Gujarati, Marathi, Tamil, Telugu, Bengali, English
- 🎨 **8 Content Vibes**: Aesthetic, Emotional, Romantic, Funny/Relatable, Short+Punchy, Storytelling, Desi/Hinglish, Inspirational
- 📱 **Platform-Optimized**: Instagram Reels, YouTube Shorts, Instagram Posts
- ⚡ **Fast Generation**: Single AI call with optimized prompts
- 🔥 **Trending Styles**: Current Indian social media trends

## Setup

1. **Install dependencies:**
```bash
npm install
```

2. **Configure API Key:**
   - Copy `.env.example` to `.env`
   - Add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_actual_api_key_here
   ```

3. **Run development server:**
```bash
npm run dev
```

4. **Open in browser:**
   - Navigate to `http://localhost:3000`
   - Fill in the form and generate content packs!

## API Endpoints

### POST /api/generate
Generate a content pack based on user preferences.

**Request Body:**
```json
{
  "topic": "morning routine",
  "language": ["Hindi", "Hinglish"],
  "vibe": ["aesthetic", "short+punchy"],
  "platform": "Instagram Reels",
  "includeScript": true
}
```

### GET /api/trends/today
Get current trending content styles (5-7 styles, cached for 1 hour).

## Testing

Run tests:
```bash
npm test
```

Run tests in watch mode:
```bash
npm run test:watch
```

## Build for Production

```bash
npm run build
npm start
```

## Project Structure

```
src/
├── types/          # TypeScript type definitions
├── validation/     # Input validation logic
├── ai/            # AI prompt engine and response parser
├── api/           # Express API server
├── data/          # Trending styles data
└── server.ts      # Main entry point

public/            # Frontend HTML/CSS/JS
```

## Requirements

- Node.js 18+
- OpenAI API key
- npm or yarn

## License

MIT
