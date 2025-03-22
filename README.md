# Jungle Safari E-commerce Backend

This is the backend API for the Jungle Safari e-commerce platform.

## Setup Instructions

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in the root directory with the following variables:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/jungle-safari
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
NODE_ENV=development
```

3. Start the development server:
```bash
npm run dev
```

## API Endpoints

### Authentication
- POST /api/auth/register - Register a new user
- POST /api/auth/login - Login user
- GET /api/auth/profile - Get user profile
- PUT /api/auth/profile - Update user profile

### Products
- GET /api/products - Get all products
- GET /api/products/:id - Get single product
- POST /api/products - Create product (admin only)
- PUT /api/products/:id - Update product (admin only)
- DELETE /api/products/:id - Delete product (admin only)
- POST /api/products/:id/ratings - Add product rating

### Categories
- GET /api/categories - Get all categories
- GET /api/categories/:id - Get single category
- POST /api/categories - Create category (admin only)
- PUT /api/categories/:id - Update category (admin only)
- DELETE /api/categories/:id - Delete category (admin only)
- GET /api/categories/:id/subcategories - Get subcategories

### Orders
- GET /api/orders/my-orders - Get user's orders
- GET /api/orders/:id - Get single order
- POST /api/orders - Create new order
- PUT /api/orders/:id/status - Update order status (admin only)
- GET /api/orders - Get all orders (admin only)

### Cart
- GET /api/cart - Get cart items
- POST /api/cart/add - Add item to cart
- PUT /api/cart/update/:productId - Update cart item quantity
- DELETE /api/cart/remove/:productId - Remove item from cart
- DELETE /api/cart/clear - Clear cart 