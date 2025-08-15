# Laravel 12 Livewire Starter Kit with Social Authentication

A modern Laravel 12 application with Livewire 3, Volt components, and social authentication capabilities. This starter kit provides a solid foundation for building SaaS applications with advanced user management and security features.

## 🚀 Features

- **Laravel 12** - Latest Laravel framework with typed routes, models, and requests
- **Livewire 3** - Full-stack framework for Laravel with real-time components
- **Volt** - Modern component syntax for Livewire
- **Social Authentication** - OAuth integration with multiple providers
- **Role-Based Access Control** - Admin, Reseller, Customer, and Agent roles
- **Multi-Tenant Support** - UUID-based user management
- **Security Features** - IP blocking, rate limiting, and security headers
- **Email Verification** - Built-in email verification system
- **Password Management** - Reset, confirmation, and secure validation
- **Modern UI** - Clean, responsive design with Tailwind CSS
- **Testing** - Comprehensive test suite with Pest PHP

## 📋 Requirements

- PHP 8.2+
- Composer
- Node.js & NPM
- SQLite (default) or MySQL/PostgreSQL
- Git

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd serveradmin
   ```

2. **Install PHP dependencies**
   ```bash
   composer install
   ```

3. **Install Node.js dependencies**
   ```bash
   npm install
   ```

4. **Environment setup**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Configure your database**
   Edit `.env` file and set your database credentials:
   ```env
   DB_CONNECTION=sqlite
   DB_DATABASE=/path/to/database.sqlite
   ```

6. **Run migrations and seeders**
   ```bash
   php artisan migrate
   php artisan db:seed
   ```

7. **Build assets**
   ```bash
   npm run build
   ```

8. **Start the development server**
   ```bash
   php artisan serve
   ```

## 🔧 Configuration

### Social Authentication

Configure your OAuth providers in the `.env` file:

```env
# Google OAuth
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
GOOGLE_REDIRECT_URI=http://localhost:8000/auth/google/callback

# GitHub OAuth
GITHUB_CLIENT_ID=your-github-client-id
GITHUB_CLIENT_SECRET=your-github-client-secret
GITHUB_REDIRECT_URI=http://localhost:8000/auth/github/callback
```

### Security Settings

The application includes several security features:

- **IP Blocking** - Configure in `config/security.php`
- **Rate Limiting** - API rate limiting with configurable thresholds
- **Security Headers** - Automatic security header injection
- **Password Policies** - Strong password validation rules

## 📁 Project Structure

```
serveradmin/
├── app/
│   ├── Console/Commands/     # Artisan commands
│   ├── Http/
│   │   ├── Controllers/      # Application controllers
│   │   └── Middleware/       # Custom middleware
│   ├── Livewire/            # Livewire components
│   ├── Models/              # Eloquent models
│   └── Providers/           # Service providers
├── config/                  # Configuration files
├── database/
│   ├── migrations/          # Database migrations
│   ├── seeders/            # Database seeders
│   └── factories/          # Model factories
├── resources/
│   ├── views/              # Blade templates
│   ├── css/                # Stylesheets
│   └── js/                 # JavaScript files
├── routes/                 # Route definitions
└── tests/                  # Test files
```

## 🎯 Key Components

### Authentication System
- Multi-provider social authentication
- Email verification workflow
- Password reset functionality
- Role-based authorization

### Admin Dashboard
- User management interface
- Account locking/unlocking
- Security monitoring
- Analytics and reporting

### Livewire Components
- Real-time form validation
- Dynamic UI updates
- Interactive dashboards
- Modal dialogs and notifications

## 🧪 Testing

Run the test suite:

```bash
# Run all tests
php artisan test

# Run specific test files
php artisan test tests/Feature/Auth/

# Run with coverage
php artisan test --coverage
```

## 🔒 Security Features

- **CSRF Protection** - Automatic CSRF token validation
- **XSS Prevention** - Input sanitization and output escaping
- **SQL Injection Protection** - Eloquent ORM with parameter binding
- **Session Security** - Secure session configuration
- **File Upload Security** - Validated file uploads
- **API Security** - Token-based authentication with Sanctum

## 🚀 Deployment

### Production Checklist

1. **Environment Configuration**
   ```bash
   APP_ENV=production
   APP_DEBUG=false
   APP_URL=https://yourdomain.com
   ```

2. **Cache Configuration**
   ```bash
   php artisan config:cache
   php artisan route:cache
   php artisan view:cache
   ```

3. **Database Optimization**
   ```bash
   php artisan migrate --force
   ```

4. **Asset Compilation**
   ```bash
   npm run build
   ```

## 📝 API Documentation

The application provides RESTful APIs for:

- User authentication and management
- Role and permission management
- Account operations
- Security monitoring

API endpoints are protected with Laravel Sanctum tokens.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:

- Create an issue in the repository
- Check the Laravel documentation
- Review the Livewire documentation

## 🔄 Changelog

### Version 1.0.0
- Initial release with Laravel 12
- Livewire 3 integration
- Social authentication
- Role-based access control
- Security middleware
- Admin dashboard
- Comprehensive test suite

---

**Built with ❤️ using Laravel 12, Livewire 3, and modern web technologies.**
