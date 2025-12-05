# 🍔 Restaurant Orders Full-Stack Application

A modern, full-stack restaurant ordering system with real-time order tracking, stunning UI, and complete order management capabilities.

## ✨ Features

### Customer Features
- 🍽️ **Beautiful Menu Display** - Browse menu items with categories and filters
- 🛒 **Smart Shopping Cart** - Add, remove, and manage items with persistent storage
- 📱 **Real-time Order Tracking** - Live updates on order status
- 🎨 **Premium UI** - Modern design with glassmorphism and smooth animations
- 💳 **Easy Checkout** - Simple order placement with customer details

### Admin Features
- 📋 **Order Management** - View and manage all orders in real-time
- 🔄 **Status Updates** - Update order status (pending → preparing → ready → completed)
- 🍕 **Menu CRUD** - Add, edit, and delete menu items
- 🔔 **Live Notifications** - Real-time alerts for new orders
- 📊 **Order Filtering** - Filter orders by status

## 🚀 Tech Stack

- **Backend**: Node.js + Express
- **Database**: SQLite3
- **Real-time**: WebSocket (ws)
- **Frontend**: Vanilla HTML/CSS/JavaScript
- **Authentication**: Session-based with bcrypt

## 📦 Installation

1. **Navigate to the backend directory**:
   ```bash
   cd C:\Users\useer\.gemini\antigravity\scratch\restaurant-orders-app\backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

## 🎯 Running the Application

1. **Start the server**:
   ```bash
   cd C:\Users\useer\.gemini\antigravity\scratch\restaurant-orders-app\backend
   npm start
   ```

2. **Access the application**:
   - **Customer Interface**: http://localhost:3000
   - **Admin Dashboard**: http://localhost:3000/admin.html

## 🔐 Default Admin Credentials

- **Username**: `admin`
- **Password**: `admin123`

## 📱 Usage

### For Customers

1. Visit http://localhost:3000
2. Browse the menu and filter by category
3. Add items to your cart
4. Click "Cart" to review your order
5. Click "Proceed to Checkout"
6. Fill in your details and place the order
7. Track your order status in real-time

### For Admins

1. Visit http://localhost:3000/admin.html
2. Login with admin credentials
3. View incoming orders in real-time
4. Update order status as you prepare them
5. Manage menu items (add, edit, delete)

## 🗄️ Database Schema

The application uses SQLite with the following tables:

- **users** - Admin user accounts
- **menu_items** - Restaurant menu items
- **orders** - Customer orders
- **order_items** - Items in each order

## 🎨 Design Features

- **Vibrant Gradients** - Purple, pink, and blue color scheme
- **Glassmorphism** - Modern translucent card designs
- **Smooth Animations** - Hover effects and transitions
- **Responsive Layout** - Works on desktop and mobile
- **Premium Typography** - Poppins font family

## 🔄 Real-time Features

The application uses WebSocket for real-time updates:

- New orders appear instantly in admin dashboard
- Order status updates reflect immediately for customers
- Menu changes sync across all clients

## 📂 Project Structure

```
restaurant-orders-app/
├── backend/
│   ├── server.js          # Express server & API routes
│   ├── database.js        # Database setup & seed data
│   ├── package.json       # Dependencies
│   └── restaurant.db      # SQLite database (auto-created)
└── frontend/
    ├── index.html         # Customer interface
    ├── styles.css         # Customer styles
    ├── app.js            # Customer logic
    ├── admin.html        # Admin dashboard
    ├── admin.css         # Admin styles
    └── admin.js          # Admin logic
```

## 🛠️ API Endpoints

### Authentication
- `POST /api/auth/login` - Admin login
- `POST /api/auth/logout` - Logout
- `GET /api/auth/session` - Check session

### Menu
- `GET /api/menu` - Get all menu items
- `GET /api/menu/:id` - Get single item
- `POST /api/menu` - Create item (admin)
- `PUT /api/menu/:id` - Update item (admin)
- `DELETE /api/menu/:id` - Delete item (admin)

### Orders
- `GET /api/orders` - Get all orders (admin)
- `GET /api/orders/:id` - Get single order
- `POST /api/orders` - Create order
- `PUT /api/orders/:id/status` - Update status (admin)

## 🎯 Sample Menu Items

The database comes pre-seeded with 12 menu items across categories:
- Burgers (Classic, Cheeseburger, Veggie)
- Pizza (Margherita, Pepperoni, BBQ Chicken)
- Salads (Caesar, Greek)
- Sides (Fries, Onion Rings)
- Drinks (Coca Cola, Lemonade)

## 🔧 Customization

### Adding New Categories
Edit the category dropdown in `admin.html` and add your category option.

### Changing Colors
Modify CSS variables in `styles.css` and `admin.css`:
```css
:root {
  --primary: #667eea;
  --secondary: #764ba2;
  /* ... */
}
```

### Changing Port
Edit `server.js`:
```javascript
const PORT = 3000; // Change to your desired port
```

## 🐛 Troubleshooting

**Port already in use**:
```bash
# Find and kill the process using port 3000
netstat -ano | findstr :3000
taskkill /PID <PID> /F
```

**Database errors**:
Delete `restaurant.db` and restart the server to recreate the database.

**WebSocket connection issues**:
Ensure the server is running and check browser console for errors.

## 📄 License

This project is open source and available for personal and commercial use.

## 🙏 Credits

Built with ❤️ for food lovers everywhere.

---

**Enjoy your restaurant ordering system! 🎉**
