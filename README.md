# 🤖 AI Meeting Notes Summarizer

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20Site-blue?style=for-the-badge)](https://meeting-notes-ai.windsurf.build)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-black?style=for-the-badge&logo=github)](https://github.com/shreeyavemula/meeting-notes-ai)

An AI-powered full-stack application that transforms meeting transcripts into structured summaries with intelligent email sharing capabilities.

## 🚀 Live Demo

**🌐 Production URL**: [https://meeting-notes-ai.windsurf.build](https://meeting-notes-ai.windsurf.build)

## ✨ Features

- **📝 Transcript Processing**: Paste meeting transcripts directly into the interface
- **🎯 Custom AI Prompts**: Tailor summaries with specific instructions (e.g., "Summarize for executives", "Highlight action items")
- **🤖 AI-Powered Summarization**: Fast, accurate summaries using Groq's LLaMA models
- **✏️ Editable Summaries**: Modify generated summaries before sharing
- **📧 Smart Email Sharing**: Opens default email client with pre-filled content
- **📱 Responsive Design**: Works seamlessly on desktop and mobile devices

## 🛠️ Tech Stack

### Backend
- **Node.js** with Express.js
- **Groq SDK** for AI summarization (LLaMA 3 8B model)
- **Netlify Functions** for serverless deployment

### Frontend
- **Vanilla HTML/CSS/JavaScript** (lightweight and fast)
- **Responsive CSS Grid/Flexbox** layout
- **Modern ES6+** JavaScript features

### Deployment & Infrastructure
- **Frontend**: Netlify (Static hosting with serverless functions)
- **AI Service**: Groq Cloud API
- **Email**: mailto protocol (browser-native)

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ installed
- Groq API account (free tier available)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/shreeyavemula/meeting-notes-ai.git
   cd meeting-notes-ai
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Update `.env` with your credentials:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   EMAIL_USER=your_email@gmail.com
   EMAIL_PASS=your_gmail_app_password
   PORT=3000
   ```

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open in browser**
   ```
   http://localhost:3000
   ```

## 🔑 Environment Variables Setup

### Groq API Key
1. Visit [Groq Console](https://console.groq.com/)
2. Sign up for a free account
3. Generate an API key
4. Add to your `.env` file

### Email Configuration (Optional)
The app uses mailto links by default. For server-side email:
1. Enable 2FA on your Gmail account
2. Generate app password: [Google App Passwords](https://myaccount.google.com/apppasswords)
3. Add credentials to `.env` file

## 📖 Usage Guide

1. **Upload Transcript**: Paste your meeting notes or call transcript
2. **Add Instructions**: Optionally specify how you want the summary formatted
3. **Generate Summary**: Click to get AI-powered summary
4. **Edit & Refine**: Modify the generated summary as needed
5. **Share**: Click to open email client with pre-filled summary

### Example Custom Prompts
- `"Summarize in bullet points for executives"`
- `"Extract only action items and deadlines"`
- `"Create a brief overview for team members"`
- `"Highlight key decisions and next steps"`

## 🏗️ Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Frontend      │    │  Netlify         │    │   Groq API      │
│   (HTML/CSS/JS) │───▶│  Functions       │───▶│   (LLaMA 3)     │
│                 │    │  (Node.js)       │    │                 │
└─────────────────┘    └──────────────────┘    └─────────────────┘
         │                                              
         ▼                                              
┌─────────────────┐                                     
│  Email Client   │                                     
│  (mailto://)    │                                     
└─────────────────┘                                     
```

## 🚀 Deployment

### Netlify Deployment (Recommended)

1. **Fork this repository**
2. **Connect to Netlify**:
   - Go to [Netlify](https://netlify.com)
   - Click "New site from Git"
   - Select your forked repository
3. **Configure environment variables** in Netlify dashboard
4. **Deploy automatically** on every push

### Manual Deployment

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login and deploy
netlify login
netlify deploy --prod
```

## 📁 Project Structure

```
meeting-notes-ai/
├── public/                 # Frontend assets
│   ├── index.html         # Main HTML file
│   ├── style.css          # Styling
│   └── script.js          # Frontend JavaScript
├── netlify/
│   └── functions/         # Serverless functions
│       ├── summarize.js   # AI summarization endpoint
│       └── share.js       # Email sharing endpoint
├── server.js              # Local development server
├── package.json           # Dependencies and scripts
├── netlify.toml          # Netlify configuration
└── README.md             # This file
```

## 🔧 API Endpoints

### Local Development
- `GET /` - Serve frontend
- `POST /api/summarize` - Generate AI summary
- `POST /api/share` - Share summary via email

### Production (Netlify Functions)
- `POST /.netlify/functions/summarize` - Generate AI summary
- `POST /.netlify/functions/share` - Share summary via email

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Groq** for providing fast AI inference
- **Netlify** for seamless deployment platform
- **LLaMA** models for powerful language understanding

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on [GitHub](https://github.com/shreeyavemula/meeting-notes-ai/issues)
- Check the [live demo](https://meeting-notes-ai.windsurf.build) for reference

---

**Built with ❤️ using modern web technologies**
