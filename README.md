# 💬 Real-Time Chat Application

A modern real-time chat app built with Node.js, Express.js, and Socket.IO featuring instant messaging, typing indicators, and a sleek gradient UI.

![Node.js](https://img.shields.io/badge/node-%3E%3D14.0.0-brightgreen) ![License](https://img.shields.io/badge/license-ISC-blue)

## ✨ Features

- ⚡ **Real-time messaging** with WebSocket
- 👤 **Username identification** 
- ⌨️ **Typing indicators**
- 🔔 **Join/leave notifications**
- 📊 **Online user counter**
- 🎨 **Modern gradient UI** with smooth animations
- 📱 **Fully responsive** design
- 🔒 **XSS protection**

## 🚀 Quick Start

### Prerequisites
- [Node.js](https://nodejs.org/) v14+ and npm

### Installation

```bash
# Clone the repository
git clone https://github.com/Kunalpantawane/realtime-chat.git
cd chat_app

# Install dependencies
npm install

# Start the server
npm start
```

Open [http://localhost:3000](http://localhost:3000) in your browser. Open multiple tabs to test real-time chat!


## 📁 Project Structure

```
chat_app/
├── public/
│   ├── index.html    # Chat interface
│   └── style.css     # Styling
├── server.js         # Express + Socket.IO server
└── package.json      # Dependencies
```

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js, Socket.IO
- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Real-time**: WebSocket (Socket.IO)

## 💻 Development

```bash
# Run with auto-reload
npm run dev

# Change port
PORT=8080 npm start
```

## 🚀 Deployment

Works on: **Heroku**, **Render**, **Railway**, **DigitalOcean**, **AWS EC2**

⚠️ Avoid: Vercel/Netlify (Socket.IO needs persistent connections)

## 📚 Core Concepts

### Socket.IO Events
```javascript
// Server → All clients
io.emit('chat message', data)

// Server → All except sender  
socket.broadcast.emit('user joined')

// Client → Server
socket.emit('chat message', { message })
```

### Key Features
- **Broadcasting**: Messages sent to all connected users
- **Typing indicators**: Debounced (1s) to reduce traffic
- **User tracking**: In-memory Map (socket ID → username)
- **XSS protection**: HTML escaping on client side

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| Port in use | `PORT=8080 npm start` |
| Module not found | `npm install` |
| Messages not showing | Check browser console (F12) |
| Can't connect | Ensure server is running |

## 🔒 Security Notes

✅ XSS protection  
✅ Input length limits  
⚠️ No authentication (anyone can join)  
⚠️ No rate limiting  
⚠️ Messages not encrypted  

**For production**: Add authentication, HTTPS, rate limiting, and database storage.

## 🎯 Future Enhancements

- [ ] Message persistence (MongoDB/PostgreSQL)
- [ ] Private messaging
- [ ] File sharing & emoji support
- [ ] User authentication
- [ ] Multiple chat rooms
- [ ] Dark mode

## 📄 License

ISC License

## 🤝 Contributing

Contributions welcome! Fork the repo, create a feature branch, and submit a PR.

## 📞 Contact

**Author**: Kunal  
**GitHub**: [@Kunalpantawane](https://github.com/Kunalpantawane)

---

⭐ Star this repo if you find it helpful!

**Built with ❤️ using Node.js, Express.js, and Socket.IO**
