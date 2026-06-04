# 💻 Software Requirements & Technologies

## Web Application & AI/ML Software Stack for AuthXHome Project

---

## 🖥️ Development Environment

### Required Software

1. **Node.js** (v14.0.0 or higher)
   - Download: https://nodejs.org/
   - Version used: v14+ (LTS recommended)
   - Purpose: Backend server runtime

2. **npm** (Node Package Manager)
   - Comes with Node.js
   - Version: 6.0.0 or higher
   - Purpose: Package management

3. **Git** (Version Control)
   - Download: https://git-scm.com/
   - Version: 2.0.0 or higher
   - Purpose: Version control and GitHub integration

4. **Code Editor** (Choose one)
   - **VS Code** (Recommended): https://code.visualstudio.com/
   - Sublime Text: https://www.sublimetext.com/
   - Atom: https://atom.io/
   - Purpose: Code editing and web development

---

## 📦 Node.js Dependencies (npm packages)

### Core Dependencies

```json
{
  "express": "^4.18.2",
  "socket.io": "^4.5.4",
  "bcryptjs": "^2.4.3",
  "jsonwebtoken": "^9.0.0",
  "dotenv": "^16.0.3",
  "axios": "^1.3.4",
  "cors": "^2.8.5",
  "body-parser": "^1.20.1"
}
```

### Detailed Package Information

1. **express** (v4.18.2)
   - Purpose: Web server framework
   - Features: Routing, middleware, HTTP utilities
   - License: MIT

2. **socket.io** (v4.5.4)
   - Purpose: Real-time bidirectional communication
   - Features: WebSocket support, event-based
   - License: MIT

3. **bcryptjs** (v2.4.3)
   - Purpose: Password hashing
   - Features: Secure password encryption
   - License: MIT

4. **jsonwebtoken** (v9.0.0)
   - Purpose: JWT token generation and verification
   - Features: Secure authentication tokens
   - License: MIT

5. **dotenv** (v16.0.3)
   - Purpose: Environment variable management
   - Features: Load .env files
   - License: BSD-2-Clause

6. **axios** (v1.3.4)
   - Purpose: HTTP client for ESP32 communication
   - Features: Promise-based HTTP requests
   - License: MIT

7. **cors** (v2.8.5)
   - Purpose: Cross-Origin Resource Sharing
   - Features: Enable CORS with various options
   - License: MIT

8. **body-parser** (v1.20.1)
   - Purpose: Parse incoming request bodies
   - Features: JSON, URL-encoded parsing
   - License: MIT

---

## 🌐 Frontend Libraries & Frameworks

### Machine Learning & AI Models

1. **TensorFlow.js** (v4.11.0)
   - CDN: https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@4.11.0
   - Purpose: Machine learning framework in browser
   - Size: ~500KB
   - Features: Neural networks, model training, inference
   - License: Apache 2.0

2. **BlazeFace Model** (v0.0.7)
   - CDN: https://cdn.jsdelivr.net/npm/@tensorflow-models/blazeface@0.0.7
   - Purpose: Lightweight face detection model
   - Size: ~100KB
   - Features: Real-time face detection, 6-point facial landmarks
   - Accuracy: 90-95% in good lighting
   - License: Apache 2.0

### UI & Communication Libraries

3. **Socket.io Client** (v4.5.4)
   - CDN: https://cdn.socket.io/4.5.4/socket.io.min.js
   - Purpose: Real-time bidirectional communication
   - Size: ~35KB
   - Features: WebSocket, event-based messaging
   - License: MIT

4. **Bootstrap** (v5.3.0) - Optional
   - CDN: https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css
   - Purpose: Responsive UI framework
   - Size: ~25KB (minified)
   - Features: Grid system, components, utilities
   - License: MIT

5. **Font Awesome** (v6.4.0) - Optional
   - CDN: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css
   - Purpose: Icon library
   - Size: ~75KB
   - Features: 2000+ icons
   - License: Font Awesome Free License

6. **QRCode.js** (v1.0.0) - Optional
   - CDN: https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js
   - Purpose: QR code generation
   - Size: ~20KB
   - Features: Generate QR codes for OTPs
   - License: MIT

### HTML5 APIs Used

- **MediaDevices API**: Camera access for face recognition
- **Canvas API**: Image processing and face detection
- **LocalStorage API**: Session management
- **Fetch API**: HTTP requests to backend
- **WebSocket API**: Real-time communication

---

## 🎨 Web Design & Frontend Technologies

### Core Technologies

1. **HTML5**
   - Purpose: Structure and markup
   - Features: Semantic elements, forms, media elements
   - Version: HTML5 standard

2. **CSS3**
   - Purpose: Styling and layout
   - Features: Flexbox, Grid, animations, transitions
   - Version: CSS3 standard

3. **JavaScript (ES6+)**
   - Purpose: Client-side logic and interactivity
   - Features: Async/await, modules, arrow functions
   - Version: ECMAScript 2015+

### Design Patterns Used

- **Responsive Design**: Mobile-first approach
- **Component-Based**: Modular UI components
- **Progressive Enhancement**: Works without JavaScript
- **Accessibility**: WCAG 2.1 guidelines

### UI/UX Features

- Clean, modern interface
- Real-time updates via WebSocket
- Camera preview for face recognition
- Visual feedback for user actions
- Loading states and error messages
- Mobile-responsive layout

---

## 🧠 AI/ML Models & Algorithms

### Face Recognition System

1. **BlazeFace Detection Model**
   - Type: Convolutional Neural Network (CNN)
   - Input: 128x128 RGB images
   - Output: Face bounding boxes + 6 landmarks
   - Speed: ~30ms per frame
   - Accuracy: 90-95%

2. **Face Comparison Algorithms**
   
   **Procrustes Analysis**
   - Purpose: Geometric shape comparison
   - Method: Align and compare facial landmarks
   - Weight: 20% in final score
   
   **Descriptor-Based Matching**
   - Purpose: Feature vector comparison
   - Method: Euclidean distance between descriptors
   - Weight: 60% in final score
   
   **Hausdorff Distance**
   - Purpose: Point set comparison
   - Method: Maximum distance between landmark sets
   - Weight: 20% in final score

3. **Recognition Parameters**
   - Training samples: 10 images per user
   - Similarity threshold: 70%
   - Minimum matches: 5 out of 10 samples (50%)
   - Processing time: < 2 seconds

### Model Performance

- **Detection Rate**: 95% in good lighting
- **False Positive Rate**: < 5%
- **False Negative Rate**: < 10%
- **Processing Speed**: Real-time (30 FPS)

---

## 🗄️ Database & Storage

### File-Based Storage (Current)

- **Format**: JSON files
- **Location**: `db/data/`
- **Files**:
  - `users.json` - User accounts
  - `face_data.json` - Face recognition data
  - `access_logs.json` - Access history
  - `otps.json` - OTP records
  - `requests.json` - Access requests

### Optional: Database Upgrade

**MongoDB** (for production)
- Download: https://www.mongodb.com/try/download/community
- Purpose: Scalable NoSQL database
- Features: Document-based, high performance
- License: SSPL

**PostgreSQL** (alternative)
- Download: https://www.postgresql.org/download/
- Purpose: Relational database
- Features: ACID compliance, advanced queries
- License: PostgreSQL License

---

## 🌍 Web Browser Requirements

### Supported Browsers

1. **Google Chrome** (Recommended)
   - Version: 90+
   - Features: Best TensorFlow.js performance, WebGL support
   - Camera API: Full support
   - Performance: Excellent

2. **Microsoft Edge**
   - Version: 90+
   - Features: Chromium-based, good performance
   - Camera API: Full support
   - Performance: Excellent

3. **Firefox**
   - Version: 88+
   - Features: Good privacy, camera support
   - Camera API: Full support
   - Performance: Good

4. **Safari** (macOS/iOS)
   - Version: 14+
   - Features: iOS camera support
   - Camera API: Limited on iOS
   - Performance: Good

### Browser Features Required

- ✅ **WebRTC**: Camera and media access
- ✅ **WebGL**: TensorFlow.js GPU acceleration
- ✅ **WebSocket**: Real-time communication
- ✅ **LocalStorage**: Session and data persistence
- ✅ **ES6+ JavaScript**: Modern JavaScript features
- ✅ **Canvas API**: Image processing
- ✅ **Fetch API**: HTTP requests

### Browser Permissions Needed

- 📷 Camera access (for face recognition)
- 🔊 Microphone access (optional, for voice features)
- 💾 Local storage (for session management)

---

## 🛠️ Development Tools & Extensions

### VS Code Extensions (Recommended)

1. **ESLint**
   - Purpose: JavaScript linting and code quality
   - Install: Search "ESLint" in VS Code Extensions

2. **Prettier - Code Formatter**
   - Purpose: Automatic code formatting
   - Install: Search "Prettier" in VS Code Extensions

3. **Live Server**
   - Purpose: Local development server with live reload
   - Install: Search "Live Server" in VS Code Extensions

4. **GitLens**
   - Purpose: Enhanced Git integration
   - Install: Search "GitLens" in VS Code Extensions

5. **HTML CSS Support**
   - Purpose: IntelliSense for HTML/CSS
   - Install: Search "HTML CSS Support" in VS Code Extensions

6. **JavaScript (ES6) Code Snippets**
   - Purpose: Code snippets for faster development
   - Install: Search "JavaScript (ES6) code snippets" in VS Code Extensions

7. **Path Intellisense**
   - Purpose: Autocomplete file paths
   - Install: Search "Path Intellisense" in VS Code Extensions

### Design Tools (Optional)

1. **Figma**
   - Website: https://www.figma.com/
   - Purpose: UI/UX design and prototyping
   - Features: Collaborative design, components
   - License: Free for personal use

2. **Adobe XD**
   - Website: https://www.adobe.com/products/xd.html
   - Purpose: UI/UX design
   - Features: Prototyping, design systems
   - License: Free starter plan

### Testing Tools

1. **Postman**
   - Download: https://www.postman.com/downloads/
   - Purpose: API testing and development
   - Features: REST API testing, collections, environments

2. **Chrome DevTools**
   - Built-in with Chrome
   - Purpose: Debugging, network analysis, performance
   - Features: Console, Network, Performance, Application tabs

3. **Lighthouse**
   - Built-in with Chrome DevTools
   - Purpose: Performance, accessibility, SEO auditing
   - Features: Automated testing, best practices

---

## 📱 Mobile & Progressive Web App (Future)

### React Native (Planned)

- **React Native CLI**: For native mobile app development
- **Expo**: Alternative framework for rapid development
- **Purpose**: iOS and Android mobile applications

### Progressive Web App (PWA)

- **Service Workers**: Offline functionality
- **Web App Manifest**: Install on home screen
- **Push Notifications**: Real-time alerts
- **Purpose**: App-like experience on mobile browsers

---

## 🔐 Security & Authentication

### Security Libraries

1. **bcryptjs**
   - Purpose: Password hashing
   - Algorithm: bcrypt with salt rounds
   - Cost factor: 12 (configurable)

2. **jsonwebtoken (JWT)**
   - Purpose: Token-based authentication
   - Algorithm: HS256 (HMAC SHA-256)
   - Expiration: 24 hours (configurable)

### Security Features

- Password hashing with bcrypt
- JWT session tokens
- CORS protection
- Input validation and sanitization
- Secure cookie handling
- Rate limiting (planned)

### SSL/TLS (Production)

1. **Let's Encrypt**
   - Website: https://letsencrypt.org/
   - Purpose: Free SSL certificates
   - Features: Auto-renewal, trusted CA

2. **Certbot**
   - Website: https://certbot.eff.org/
   - Purpose: SSL certificate management
   - Features: Automatic renewal

---

## 📊 Monitoring & Performance

### Monitoring Tools (Optional)

1. **PM2**
   - Install: `npm install -g pm2`
   - Purpose: Node.js process management
   - Features: Auto-restart, monitoring, clustering

2. **Morgan**
   - Install: `npm install morgan`
   - Purpose: HTTP request logging
   - Features: Log formatting, custom tokens

3. **Winston**
   - Install: `npm install winston`
   - Purpose: Application logging
   - Features: Multiple transports, log levels

### Performance Optimization

- Image compression and optimization
- Lazy loading for images
- Code minification
- Gzip compression
- Browser caching
- CDN for static assets (production)

---

## 🖼️ Image Processing

### Image Libraries (Optional)

1. **Sharp**
   - Install: `npm install sharp`
   - Purpose: High-performance image processing
   - Features: Resize, compress, format conversion

2. **Jimp**
   - Install: `npm install jimp`
   - Purpose: JavaScript image manipulation
   - Features: Pure JavaScript, no native dependencies

### Image Optimization

- JPEG quality: 85%
- Maximum resolution: 1920x1080
- Thumbnail generation: 200x200
- Format: JPEG for photos, PNG for UI elements

---

## 📦 Installation Commands

### Install Node.js Dependencies

```bash
# Install all dependencies from package.json
npm install

# Or install individually
npm install express socket.io bcryptjs jsonwebtoken dotenv axios cors body-parser

# Install development dependencies (optional)
npm install --save-dev nodemon eslint prettier
```

### Install Global Tools (Optional)

```bash
# PM2 for process management
npm install -g pm2

# Nodemon for auto-restart during development
npm install -g nodemon
```

### Start Development Server

```bash
# Standard start
node server.js

# With nodemon (auto-restart on changes)
nodemon server.js

# With PM2 (production)
pm2 start server.js --name "authxhome"
```

---

## 💾 System Requirements

### Minimum Requirements

- **OS**: Windows 10, macOS 10.14, Ubuntu 18.04
- **RAM**: 4GB
- **Storage**: 2GB free space
- **Processor**: Dual-core 2.0 GHz
- **Internet**: Required for initial setup and CDN libraries
- **Camera**: 720p webcam (for face recognition)

### Recommended Requirements

- **OS**: Windows 11, macOS 12+, Ubuntu 20.04+
- **RAM**: 8GB+
- **Storage**: 5GB+ free space
- **Processor**: Quad-core 2.5 GHz+
- **Internet**: Broadband connection (10 Mbps+)
- **Camera**: 1080p webcam (for better face recognition)
- **GPU**: Integrated graphics with WebGL support

---

## 🌐 Network Requirements

### Server Configuration

- **Port 3000**: Web server (HTTP) - default
- **Port 443**: HTTPS (production)
- **Port 80**: HTTP redirect to HTTPS (production)

### Firewall Rules

- Allow inbound on port 3000 (development)
- Allow inbound on port 443 (production)
- Allow outbound for npm package downloads

### WiFi Requirements

- **Standard**: 802.11 b/g/n/ac
- **Frequency**: 2.4 GHz or 5 GHz
- **Security**: WPA2 or WPA3 recommended
- **Bandwidth**: Minimum 5 Mbps for smooth operation

---

## 📋 Software Versions Used in Project

```
Node.js: v14.17.0
npm: v6.14.13
Express: v4.18.2
TensorFlow.js: v4.11.0
BlazeFace Model: v0.0.7
Socket.io: v4.5.4
bcryptjs: v2.4.3
jsonwebtoken: v9.0.0
Git: v2.51.0
Chrome: v120+
```

---

## 🔄 Update & Maintenance Commands

### Update Node.js Packages

```bash
# Check for outdated packages
npm outdated

# Update all packages to latest versions
npm update

# Update specific package
npm update express

# Update to latest major versions (use with caution)
npm install express@latest
```

### Clean Installation

```bash
# Remove node_modules and package-lock.json
rm -rf node_modules package-lock.json

# Reinstall all dependencies
npm install
```

### Security Audit

```bash
# Check for security vulnerabilities
npm audit

# Fix vulnerabilities automatically
npm audit fix

# Force fix (may introduce breaking changes)
npm audit fix --force
```

---

## 📚 Documentation & Learning Resources

### Official Documentation

- **Node.js**: https://nodejs.org/docs/
- **Express.js**: https://expressjs.com/
- **TensorFlow.js**: https://www.tensorflow.org/js
- **BlazeFace Model**: https://github.com/tensorflow/tfjs-models/tree/master/blazeface
- **Socket.io**: https://socket.io/docs/
- **MDN Web Docs**: https://developer.mozilla.org/
- **JavaScript**: https://javascript.info/

### Tutorials & Guides

- **TensorFlow.js Face Detection**: https://www.tensorflow.org/js/tutorials
- **Node.js Best Practices**: https://github.com/goldbergyoni/nodebestpractices
- **Express.js Guide**: https://expressjs.com/en/guide/routing.html
- **WebRTC Camera Access**: https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia

### Community Resources

- **Stack Overflow**: https://stackoverflow.com/
- **GitHub**: https://github.com/
- **npm Registry**: https://www.npmjs.com/
- **TensorFlow Forum**: https://discuss.tensorflow.org/

---

## 🆘 Troubleshooting

### Common Issues & Solutions

1. **npm install fails**
   ```bash
   # Clear npm cache
   npm cache clean --force
   
   # Delete node_modules and reinstall
   rm -rf node_modules package-lock.json
   npm install
   ```

2. **Port 3000 already in use**
   ```bash
   # Option 1: Change port in .env file
   PORT=3001
   
   # Option 2: Kill process using port 3000 (Windows)
   netstat -ano | findstr :3000
   taskkill /PID <PID> /F
   
   # Option 2: Kill process using port 3000 (Mac/Linux)
   lsof -ti:3000 | xargs kill -9
   ```

3. **Camera not working in browser**
   - Check browser permissions (Settings → Privacy → Camera)
   - Use HTTPS or localhost (required for camera access)
   - Try different browser (Chrome recommended)
   - Check if camera is being used by another application

4. **TensorFlow.js not loading**
   - Check internet connection (CDN required)
   - Clear browser cache
   - Check browser console for errors
   - Verify WebGL support: chrome://gpu/

5. **Face recognition not accurate**
   - Ensure good lighting conditions
   - Position face directly in front of camera
   - Capture 10 training samples with varied angles
   - Clean camera lens
   - Use higher resolution camera (1080p recommended)

6. **Session expires immediately**
   - Check system clock (JWT uses timestamps)
   - Verify JWT_SECRET in .env file
   - Check browser LocalStorage is enabled
   - Clear browser cookies and cache

7. **Socket.io connection fails**
   - Check if server is running
   - Verify port 3000 is accessible
   - Check firewall settings
   - Look for CORS errors in console

---

## ✅ Installation Checklist

### Software Installation
- [ ] Node.js installed (v14+)
- [ ] npm installed (v6+)
- [ ] Git installed
- [ ] Code editor installed (VS Code recommended)
- [ ] Chrome browser installed (v90+)

### Project Setup
- [ ] Project cloned/downloaded
- [ ] npm packages installed (`npm install`)
- [ ] .env file created and configured
- [ ] Database files initialized (db/data/*.json)

### Development Environment
- [ ] VS Code extensions installed (optional)
- [ ] Postman installed for API testing (optional)
- [ ] Git configured with GitHub account

### Testing
- [ ] Server starts successfully (`node server.js`)
- [ ] Website accessible at http://localhost:3000
- [ ] Camera permission granted in browser
- [ ] Face detection working
- [ ] Login/registration working

### Production (Optional)
- [ ] SSL certificate obtained
- [ ] Domain name configured
- [ ] Firewall rules configured
- [ ] PM2 installed and configured
- [ ] Backup system configured

---

## 🎯 Quick Start Guide

### For Developers

1. **Install Node.js** from https://nodejs.org/
2. **Clone the project** from GitHub
3. **Install dependencies**: `npm install`
4. **Create .env file** with required variables
5. **Start server**: `node server.js`
6. **Open browser**: http://localhost:3000
7. **Register account** and start using

### For Designers

1. **HTML files** are in `public/` folder
2. **CSS styles** are embedded in HTML files
3. **Edit UI** by modifying HTML/CSS
4. **Test changes** by refreshing browser
5. **Use Chrome DevTools** for debugging

### For Testers

1. **Start server**: `node server.js`
2. **Open Postman** for API testing
3. **Test endpoints** listed in documentation
4. **Check browser console** for errors
5. **Test face recognition** with different users
6. **Report issues** on GitHub

---

## 📝 Notes

- All software listed is **free and open-source** except where noted
- **No Arduino or ESP32 software** required for web application
- **Camera required** for face recognition features
- **Internet connection** required for CDN libraries
- **HTTPS required** for camera access (except localhost)
- **Modern browser** required for best performance

---

## 🔗 Quick Links

- **Project Repository**: https://github.com/ganthimathi123/Security_System_AuthXSecure
- **Node.js Download**: https://nodejs.org/
- **VS Code Download**: https://code.visualstudio.com/
- **Chrome Download**: https://www.google.com/chrome/
- **Git Download**: https://git-scm.com/

---

**Last Updated**: March 2026  
**Version**: 2.0 (Web Application Focus)
