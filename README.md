# TalkEZ v85 - Mental Health Wellness Platform

A comprehensive mental health platform designed for college students, featuring AI-powered chatbot support, appointment booking, therapeutic games, and progress tracking.

## 🌟 Features

### Core Features
- **AI Chatbot Support**: 24/7 mental health assistance with Emma, our AI wellness companion
- **Appointment Booking**: Schedule sessions with qualified mental health professionals
- **Mind Games**: Therapeutic games designed to improve cognitive function and mental wellness
- **Progress Tracking**: Visual charts and insights to monitor your mental health journey
- **User Profiles**: Customizable profiles with privacy settings and personal information management

### v85 Enhancements
- **Interactive Tutorial**: Step-by-step onboarding for new users
- **Local Storage**: No database required - all data stored locally for privacy
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Real-time Chat**: Smooth messaging experience with typing indicators and message status
- **Energy Points System**: Gamification to encourage regular platform usage

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ or Bun
- Modern web browser with JavaScript enabled

### Installation

1. **Clone the repository**
   \`\`\`bash
   git clone <repository-url>
   cd talkez-v85
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   # or
   bun install
   \`\`\`

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   \`\`\`env
   OPENAI_API_KEY=your_openai_api_key_here
   GOOGLE_AI_API_KEY=your_google_ai_api_key_here
   JWT_SECRET=your_jwt_secret_here
   \`\`\`

4. **Run the development server**
   \`\`\`bash
   npm run dev
   # or
   bun dev
   \`\`\`

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Project Structure

\`\`\`
talkez-v85/
├── app/                          # Next.js App Router pages
│   ├── dashboard/               # Main dashboard
│   ├── profile/                 # User profile management
│   ├── chatbot/                 # AI chatbot interface
│   ├── games/                   # Mind games section
│   ├── appointment/             # Appointment booking
│   └── admin/                   # Admin dashboard
├── components/                   # Reusable React components
│   ├── ui/                      # shadcn/ui components
│   ├── tutorial/                # Tutorial system
│   ├── profile/                 # Profile-related components
│   ├── games/                   # Game components
│   └── progress/                # Progress tracking components
├── lib/                         # Utility libraries
│   ├── mongodb.ts              # Local storage mock (v85)
│   ├── jwt.ts                  # JWT utilities
│   └── local-storage.ts        # Local storage helpers
├── hooks/                       # Custom React hooks
└── public/                      # Static assets
\`\`\`

## 🎮 Available Games

### Memory Match
- **Difficulty**: Easy
- **Category**: Memory
- **Description**: Test and improve memory by matching pairs of cards

### Word Association
- **Difficulty**: Medium
- **Category**: Language
- **Description**: Strengthen vocabulary and mental connections

### Number Ninja
- **Difficulty**: Hard
- **Category**: Mathematics
- **Description**: Sharpen mental math skills with quick calculations

### Pattern Puzzle
- **Difficulty**: Medium
- **Category**: Logic
- **Description**: Solve visual puzzles by identifying patterns

## 👥 User Roles

### Students
- Access to all mental health features
- Personal progress tracking
- AI chatbot support
- Game participation and scoring

### Administrators/Counselors
- User management dashboard
- Appointment oversight
- Analytics and reporting
- System administration

### Default Admin Credentials
\`\`\`
Username: admin
Password: admin

Counselor Accounts:
- dr-nisha / admin1
- dr-lavanya / admin2
- dr-sangeetha / admin3
- dr-harikumar / admin4
\`\`\`

## 🔧 Configuration

### Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | OpenAI API key for chatbot | Yes |
| `GOOGLE_AI_API_KEY` | Google AI API key (alternative) | Optional |
| `JWT_SECRET` | Secret for JWT token signing | Yes |

### Local Storage Structure

The v85 version uses local storage instead of a database:

\`\`\`javascript
// User data
localStorage.setItem('user_profile', JSON.stringify(userProfile))

// Tutorial completion
localStorage.setItem('tutorial_completed', 'true')

// Game scores
localStorage.setItem('game_scores', JSON.stringify(scores))

// Mental health data
localStorage.setItem('mental_health_profile', JSON.stringify(profile))
\`\`\`

## 🎨 Design System

### Color Palette
- **Primary**: `#5ECFBC` (Teal)
- **Secondary**: `#FFD166` (Yellow)
- **Accent**: `#FF9F1C` (Orange)
- **Background**: `#B4E4E0` (Light Teal)
- **Text**: `#333333` (Dark Gray)

### Typography
- **Font Family**: Inter
- **Headings**: Bold, various sizes
- **Body**: Regular, 16px base

## 📱 Responsive Breakpoints

- **Mobile**: < 640px
- **Tablet**: 640px - 1024px
- **Desktop**: > 1024px

## 🔒 Privacy & Security

### Data Storage
- All user data stored locally in browser
- No server-side data persistence
- Users control their own data

### Security Features
- JWT-based authentication
- Input validation and sanitization
- XSS protection
- CSRF protection

## 🧪 Testing

### Running Tests
\`\`\`bash
npm test
# or
bun test
\`\`\`

### Test Coverage
- Component unit tests
- Integration tests for key features
- E2E tests for critical user flows

## 📦 Deployment

### Vercel (Recommended)
1. Connect your repository to Vercel
2. Set environment variables in Vercel dashboard
3. Deploy automatically on push to main branch

### Manual Deployment
\`\`\`bash
npm run build
npm start
\`\`\`

### Docker Deployment
\`\`\`bash
docker build -t talkez-v85 .
docker run -p 3000:3000 talkez-v85
\`\`\`

## 🤝 Contributing

### Development Workflow
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Code Style
- Use TypeScript for type safety
- Follow ESLint and Prettier configurations
- Write meaningful commit messages
- Add tests for new features

## 📚 API Documentation

### Chatbot API
\`\`\`typescript
POST /api/chat
{
  "messages": [
    {
      "role": "user",
      "content": "How are you feeling today?"
    }
  ]
}
\`\`\`

### Authentication API
\`\`\`typescript
POST /api/auth/login
{
  "email": "user@example.com",
  "password": "password"
}
\`\`\`

## 🐛 Troubleshooting

### Common Issues

**Tutorial not appearing**
- Clear browser cache and localStorage
- Ensure JavaScript is enabled
- Check browser console for errors

**Chatbot not responding**
- Verify OpenAI API key is set correctly
- Check network connectivity
- Review API rate limits

**Games not loading**
- Refresh the page
- Clear browser cache
- Check browser compatibility

### Browser Support
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **shadcn/ui** for the beautiful component library
- **Framer Motion** for smooth animations
- **Recharts** for data visualization
- **Lucide React** for icons
- **OpenAI** for AI capabilities

## 📞 Support

For support and questions:
- Email: support@talkez.com
- Documentation: [docs.talkez.com](https://docs.talkez.com)
- Issues: [GitHub Issues](https://github.com/your-repo/issues)

## 🗺️ Roadmap

### v86 (Planned)
- [ ] Offline mode support
- [ ] Data export/import functionality
- [ ] Advanced analytics dashboard
- [ ] Multi-language support
- [ ] Voice chat capabilities

### v87 (Future)
- [ ] Mobile app (React Native)
- [ ] Integration with wearable devices
- [ ] Advanced AI personality customization
- [ ] Group therapy sessions
- [ ] Peer support networks

---

**TalkEZ v85** - Mental Health Matters 💚

Built with ❤️ for college students and mental health awareness.
