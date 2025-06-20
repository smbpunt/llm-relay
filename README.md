# LLM Relay

A web application built with Symfony 7.3 that provides an intuitive interface for interacting with multiple Large Language Models (LLMs). Users can submit questions, receive responses, and forward them to other LLMs for validation, correction, or enrichment.

## 🚀 Key Features

- **Multi-LLM Support**: Integrate with various commercial LLM providers (OpenAI, Anthropic, Google, etc.)
- **Agent Chaining**: Forward responses between different LLMs for enhanced accuracy and insights
- **User Authentication**: Secure registration and login system
- **Conversation History**: Store and retrieve past interactions
- **Secure API Key Management**: User-provided API keys with Symfony security best practices
- **Real-time Streaming**: Support for streaming responses (when available)
- **Modern UI**: Built with Symfony UX and Bootstrap for a responsive experience

## 🛠️ Tech Stack

- **Framework**: Symfony 7.3
- **Frontend**: Twig templates with Symfony UX components
- **Asset Management**: Symfony AssetMapper (no build step required)
- **CSS Framework**: Bootstrap 5
- **Database**: PostgreSQL
- **Testing**: PHPUnit
- **Code Quality**: PHP-CS-Fixer, PHPStan, Rector
- **CI/CD**: GitLab CI

## 📋 Requirements

- PHP 8.2 or higher
- Composer
- PostgreSQL 14+
- Symfony CLI (recommended for development)

## 🔧 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone [repository-url]
   cd llm-multi-agent-platform
   ```

2. **Install dependencies**
   ```bash
   composer install
   ```

3. **Configure environment**
   ```bash
   composer dump-env prod
   ```
   Update `.env.local.php` with your database credentials:
   ```
   DATABASE_URL="postgresql://username:password@127.0.0.1:5432/llm_platform?serverVersion=14&charset=utf8"
   ```

4. **Set up the database**
   ```bash
   php bin/console doctrine:database:create
   php bin/console doctrine:migrations:migrate
   ```

5. **Install assets**
   ```bash
   php bin/console asset-map:compile
   ```

6. **Start the development server**
   ```bash
   symfony server:start
   ```

## 🚀 Usage

1. **Register/Login**: Create an account or log in to access the platform
2. **Configure API Keys**: Add your LLM provider API keys in your account settings
3. **Submit Questions**: Use the main form to submit questions to your chosen LLM
4. **Chain Responses**: Forward any response to another LLM for validation or enhancement
5. **View History**: Access your conversation history from your dashboard

## 🧪 Testing

Run the test suite:
```bash
# Unit tests
php bin/phpunit

# Code style check
php vendor/bin/php-cs-fixer fix --dry-run

# Static analysis
php vendor/bin/phpstan analyse

# Automated refactoring check
php vendor/bin/rector process --dry-run
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Coding Standards

- Follow PSR-12 coding standards
- Write PHPUnit tests for new features
- Ensure all tests pass before submitting PR
- Run code quality tools before committing

## 📄 License

[Specify your license here - e.g., MIT, GPL, proprietary]

## 📞 Support

- **Issues**: Please use the GitHub issue tracker for bug reports and feature requests
- **Documentation**: [Link to documentation]
- **Contact**: [Contact email or form]