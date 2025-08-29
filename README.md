# GSM Web Store - Professional Mobile Services Platform

A comprehensive web store for GSM services with a powerful admin panel and mini-CMS functionality.

## Features

### 🏪 **Main Storefront**
- Clean, modern landing page with hero section
- Prominent advertisement banner (customizable)
- Two rich-content CMS sections (fully editable)
- Service categories with tabbed navigation:
  - IMEI Unlock Services
  - FRP / iCloud Services  
  - Server Tools / Credits
  - Remote Services
- Samsung FRP model checker with searchable database
- Contact form with Telegram integration
- Responsive design for all devices

### 🔧 **Admin Panel**
- **Secure Access**: Hidden admin URL with multi-layer security
  - Username/password authentication
  - 2FA code verification
  - CAPTCHA protection
  - Rate limiting and lockout protection
- **Dashboard**: Overview of services, inquiries, and server status
- **Service Management**: Add, edit, delete services with pricing
- **Inquiry Management**: View and manage customer inquiries
- **CMS Editor**: Edit homepage content sections without coding
- **Advertisement Manager**: Update promo banners and scheduling
- **Media Gallery**: Upload and manage images, GIFs, videos
- **Settings Panel**: 
  - Brand configuration
  - Currency settings
  - Contact information
  - Payment gateway setup
  - Theme and font customization
- **Server Status**: Toggle service availability (MTK/SPD/QLM, Remote Flash, etc.)
- **Factory Reset**: Restore site to default configuration

### 🔒 **Security Features**
- Hidden admin URL (`/admin.html`)
- Multi-factor authentication (2FA + CAPTCHA)
- JWT-based session management
- SQLite database with prepared statements
- Input validation and sanitization
- Rate limiting on login attempts
- Secure password hashing with bcrypt

### 📱 **Samsung FRP Checker**
- Searchable model database
- Support status indication
- Pricing information
- Admin-editable model list
- Real-time search filtering

## Quick Start

### Installation
```bash
# Clone and install dependencies
npm install

# Start the development server
npm run dev

# Start the backend server (in another terminal)
npm run server
```

### Access Points
- **Main Store**: http://localhost:5173
- **FRP Checker**: http://localhost:5173/frp-checker.html  
- **Admin Panel**: http://localhost:5173/admin.html

### Default Admin Credentials
- **Username**: `admin`
- **Password**: `admin123`
- **2FA Code**: `000000` (demo mode)

## Project Structure

```
gsm-web-store/
├── index.html              # Main storefront
├── frp-checker.html        # Samsung FRP model checker
├── admin.html              # Admin panel
├── src/
│   ├── main.js            # Main storefront JavaScript
│   ├── frp-checker.js     # FRP checker functionality
│   ├── admin.js           # Admin panel logic
│   └── style.css          # Global styles
├── server/
│   └── index.js           # Express.js backend server
└── README.md
```

## Technology Stack

### Frontend
- **Vanilla JavaScript** - No framework dependencies
- **Tailwind CSS** - Utility-first styling
- **Lucide Icons** - Beautiful icon library
- **Responsive Design** - Mobile-first approach

### Backend
- **Node.js** with Express.js
- **SQLite** database for data persistence
- **JWT** for authentication
- **bcrypt** for password hashing
- **CORS** enabled for development

## Database Schema

### Services
- Service management with categories, pricing, and descriptions

### Inquiries  
- Customer inquiry tracking with timestamps

### Settings
- Site configuration and branding options

### FRP Data
- Samsung model database with support status

### Admin Users
- Secure admin account management

## Customization

### Branding
- Update brand name, colors, and logo through admin panel
- Customize contact information (Telegram, WhatsApp)
- Set currency and pricing options

### Content Management
- Edit hero section content
- Modify CMS sections with rich text
- Update advertisement banners
- Manage service categories and descriptions

### Services
- Add/edit/delete services through admin panel
- Set pricing and categories
- Upload service images
- Configure availability status

## Security Recommendations

### Production Deployment
1. **Change default admin credentials**
2. **Use strong JWT secret key**
3. **Enable HTTPS with SSL certificate**
4. **Configure Cloudflare WAF and Turnstile**
5. **Use environment variables for sensitive data**
6. **Regular database backups**
7. **Monitor login attempts and failed authentications**

### Environment Variables
```bash
JWT_SECRET=your-super-secret-jwt-key
PORT=3001
NODE_ENV=production
```

## API Endpoints

### Public APIs
- `GET /api/services` - Get all services
- `GET /api/settings` - Get site settings  
- `POST /api/inquiries` - Submit customer inquiry
- `GET /api/frp-data` - Get FRP model data

### Admin APIs (Authentication Required)
- `POST /api/admin/login` - Admin authentication
- `GET /api/admin/services` - Get services for admin
- `POST /api/admin/services` - Update services
- `GET /api/admin/inquiries` - Get customer inquiries
- `GET /api/admin/settings` - Get admin settings
- `POST /api/admin/settings` - Update settings

## Support

For technical support or customization requests:
- **Telegram**: Contact through the integrated Telegram bot
- **Documentation**: Comprehensive inline code comments
- **Demo**: Full working demo with sample data

## License

This project is designed for professional GSM service providers. All rights reserved.

---

**Built with ❤️ for the GSM community**
