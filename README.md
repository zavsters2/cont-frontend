# Contacts Manager Frontend

A clean, pastel-themed frontend for the Contacts Management API built with vanilla JavaScript, HTML, and CSS.

## Features

- User registration and login
- Create, view, edit, and delete contacts
- Beautiful pastel color scheme
- Responsive design for mobile and desktop
- Local storage for session persistence
- Toast notifications for user feedback

## Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Custom properties, Flexbox, Grid
- **Vanilla JavaScript** - No frameworks/libraries
- **Fetch API** - HTTP requests

## Screenshots

The application features a soft pastel color palette with:
- Lavender and pink gradients
- Mint and blue contact cards
- Smooth animations and hover effects

## Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- The backend API running on `http://localhost:5000`

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/contacts-frontend.git
cd contacts-frontend
```

### 2. Configure API URL (if needed)

If your backend is running on a different URL, edit `app.js` and update:

```javascript
const API_BASE_URL = 'http://localhost:5000/api';
```

### 3. Serve the application

You can use any static file server. Here are some options:

**Option A: Using Python (built-in)**
```bash
# Python 3
python -m http.server 3000

# Python 2
python -m SimpleHTTPServer 3000
```

**Option B: Using Node.js (npx)**
```bash
npx serve -p 3000
```

**Option C: Using VS Code Live Server**
- Install the "Live Server" extension
- Right-click on `index.html` and select "Open with Live Server"

**Option D: Open directly in browser**
- Simply open `index.html` in your browser (some features may be limited due to CORS)

### 4. Access the application

Open your browser and navigate to `http://localhost:3000`

## Usage

### Registration
1. Click on the "Register" tab
2. Enter your name, email, and password (min 6 characters)
3. Click "Register" to create your account

### Login
1. Enter your email and password
2. Click "Login" to access your contacts

### Managing Contacts

**Add a Contact:**
1. Fill in the contact form (name is required)
2. Click "Save Contact"

**Edit a Contact:**
1. Click the "Edit" button on a contact card
2. Modify the details in the form
3. Click "Update Contact"
4. Or click "Cancel" to discard changes

**Delete a Contact:**
1. Click the "Delete" button on a contact card
2. Confirm the deletion

### Logout
Click the "Logout" button in the header to sign out

## Project Structure

```
contacts-frontend/
├── index.html    # Main HTML file
├── styles.css    # All styles with pastel theme
├── app.js        # JavaScript application logic
└── README.md     # This file
```

## Color Palette

The application uses a carefully selected pastel color scheme:

| Color | Hex Code | Usage |
|-------|----------|-------|
| Pastel Pink | `#FFD1DC` | Contact cards, accents |
| Pastel Blue | `#A8D8EA` | Contact cards, gradients |
| Pastel Purple | `#D4A5FF` | Focus states, accents |
| Pastel Green | `#B5EAD7` | Success messages |
| Pastel Yellow | `#FFEAA7` | Empty states |
| Pastel Lavender | `#E2D1F9` | Headers, tabs |
| Pastel Mint | `#C9F0E4` | Contact cards |
| Pastel Peach | `#FFCAB0` | Contact cards |

## API Integration

The frontend connects to the following backend endpoints:

### Authentication
- `POST /api/auth/register` - Create new account
- `POST /api/auth/login` - Login user

### Contacts
- `GET /api/contacts` - Fetch all contacts
- `POST /api/contacts` - Create new contact
- `PUT /api/contacts/:id` - Update contact
- `DELETE /api/contacts/:id` - Delete contact

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Customization

### Changing Colors

Edit the CSS custom properties in `styles.css`:

```css
:root {
  --pastel-pink: #FFD1DC;
  --pastel-blue: #A8D8EA;
  /* ... other colors */
}
```

### Changing API URL

Edit the constant in `app.js`:

```javascript
const API_BASE_URL = 'http://your-api-url/api';
```

## Troubleshooting

### CORS Errors
Make sure the backend has CORS enabled for your frontend URL. The backend should be configured with:
```javascript
app.use(cors());
```

### Connection Refused
Ensure the backend server is running on `http://localhost:5000`

### Login Not Working
1. Check browser console for errors
2. Verify the backend is responding at `/api/health`
3. Clear localStorage and try again

## License

MIT
