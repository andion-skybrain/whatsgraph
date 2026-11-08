# WhatsGraph 💬

> Showcase repository. The full WhatsGraph source code is private until audited. This README documents what the app does and how it works. Screenshots coming soon.

A beautiful, privacy-first WhatsApp chat analyzer that runs entirely in your browser. Parse, display, and analyze your WhatsApp chat exports with a responsive, WhatsApp-inspired interface.

![WhatsGraph Screenshot](https://img.shields.io/badge/Privacy-100%25%20Local-brightgreen) ![License](https://img.shields.io/badge/License-MIT-blue) ![React](https://img.shields.io/badge/React-18-61dafb) ![TypeScript](https://img.shields.io/badge/TypeScript-5-3178c6)

## ✨ Features

### 📱 Beautiful Chat Display

- **WhatsApp-inspired Interface** - Familiar design with accurate bubble styling
- **Device-Specific Wallpapers** - Custom backgrounds for Mobile (9 options) and Desktop (3 options)
- **Rich Media Support** - Display images, videos, audio, and documents inline
- **Sticky Date Headers** - Context-aware chronological navigation
- **Dark/Light Mode** - Fully synced theme support with smooth transitions

### 📊 Advanced Analytics

- **Interactive Stats Panel** - Comprehensive breakdown of chat habits
- **Media Distribution** - Responsive charts showing file type usage
- **Participation Metrics** - Who talks the most, fastest response times
- **Activity Heatmaps** - Visualizing busiest times of day and week
- **Word Clouds & Emojis** - Fun insights into vocabulary and emotions

### 🔍 Powerful Search & Navigation

- **Real-time Search** - Instant results with highlighting
- **Calendar Jump** - Navigate to specific dates instantly
- **Filters** - Drill down by media type, sender, date, or content
- **Performance Mode** - Virtualized rendering for chats with 3k+ messages

### 📤 Export & Privacy

- **Multiple Formats** - Export to PDF, JSON, HTML, or Clean Text
- **Privacy First** - 100% Client-side processing. Your data **never** leaves your device.
- **Zero Tracking** - No analytics, no servers, no cookies.

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

The source code is private, so it is not included in this showcase repo. With the code, setup is the usual React flow:

```bash
# Install dependencies
npm install

# Start development server
npm run dev
```

### Building for Production

```bash
# Create production build
npm run build

# Preview production build
npm run preview
```

## 📖 Usage

### Exporting from WhatsApp

1. Open WhatsApp on your phone
2. Go to the chat you want to export
3. Tap the menu (⋮) → More → Export chat
4. Choose "Attach Media" or "Without Media"
5. Save the .zip or .txt file

### Using WhatsGraph

1. Open WhatsGraph in your browser
2. Drag & drop your exported file, or click "Choose File"
3. Alternatively, click "Check with Sample" to try with demo data
4. Explore your chat with search, filters, and statistics!

## 🏗️ Technology Stack

- **React 18** - UI framework
- **TypeScript** - Type safety
- **Zustand** - State management
- **Tailwind CSS** - Styling
- **Recharts** - Chart visualizations
- **react-window** - Virtualized lists
- **JSZip** - ZIP file extraction
- **date-fns** - Date manipulation
- **Lucide React** - Icons
- **jsPDF** - PDF generation

## 📁 Project Structure

```
src/
├── components/
│   ├── ChatView/           # Main chat display
│   │   ├── ChatView.tsx    # Container component
│   │   ├── MessageBubble.tsx
│   │   ├── MediaDisplay.tsx
│   │   ├── VirtualizedMessageList.tsx
│   │   └── StickyDateHeader.tsx
│   ├── FileUpload/         # File upload handling
│   ├── SearchBar/          # Search functionality
│   ├── StatsPanel/         # Statistics display
│   ├── FilterPanel/        # Message filtering
│   ├── ExportPanel/        # Export options
│   ├── SettingsPanel/      # App settings
│   ├── CalendarModal/      # Date navigation
│   ├── PrivacyNotice/      # Privacy information
│   ├── Tutorial/           # First-time user guide
│   ├── Toast/              # Notifications
│   ├── ConfirmDialog/      # Confirmation dialogs
│   ├── ImageLightbox/      # Full-screen image viewer
│   └── ThemeToggle/        # Dark/light mode
├── store/
│   ├── chatStore.ts        # Main app state
│   ├── audioStore.ts       # Audio playback state
│   ├── lightboxStore.ts    # Image lightbox state
│   └── tutorialStore.ts    # Tutorial progress
├── utils/
│   ├── parser.ts           # WhatsApp text parser
│   ├── zipHandler.ts       # ZIP file processing
│   ├── analytics.ts        # Statistics calculation
│   ├── sampleChat.ts       # Demo data generator
│   └── export.ts           # Export functionality
└── types/
    └── index.ts            # TypeScript definitions
```

## 🎨 Features in Detail

### Message Parsing

Supports multiple WhatsApp export formats:

- Date formats: DD/MM/YYYY, MM/DD/YYYY, YYYY-MM-DD
- Time formats: 12-hour and 24-hour
- Special messages: edited, deleted, system messages
- Media attachments: images, videos, audio, documents

### Virtualized Rendering

For chats with 3000+ messages, WhatsGraph automatically enables virtualized rendering:

- Only visible messages are rendered in the DOM
- Smooth scrolling maintained
- Audio playback persists across scroll

### Accessibility

- ARIA labels on all interactive elements
- Keyboard navigation support
- Screen reader compatible
- Focus management for modals

### Browser Support

| Browser       | Version | Status          |
| ------------- | ------- | --------------- |
| Chrome        | 88+     | ✅ Full support |
| Firefox       | ESR+    | ✅ Full support |
| Safari        | 14+     | ✅ Full support |
| Edge          | 88+     | ✅ Full support |
| Mobile Chrome | Latest  | ✅ Full support |
| Mobile Safari | 14+     | ✅ Full support |

**Notes:**

- Requires JavaScript enabled
- Uses modern APIs: File API, Blob URLs, CSS Grid/Flexbox
- Optimized for both mouse and touch input
- Safe area support for notched devices (iPhone X+)

## 🔧 Configuration

### Settings

Access settings via the ⚙️ button:

- **Theme**: Light/Dark/System
- **Font Size**: Small/Medium/Large
- **Performance Mode**: Auto/Enabled/Disabled
- **Clear Data**: Remove loaded chat

### Keyboard Shortcuts

| Shortcut        | Action                 |
| --------------- | ---------------------- |
| `Ctrl/Cmd + F`  | Focus search           |
| `Enter`         | Next search result     |
| `Shift + Enter` | Previous search result |
| `Esc`           | Close modals/lightbox  |

## 🤝 Contributing

Contributions are welcome! Please read our contributing guidelines before submitting a PR.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- WhatsApp for the beautiful UI inspiration
- The React community for amazing tools
- All contributors and testers

---

<p align="center">
  Made with ❤️ for privacy-conscious users
</p>
