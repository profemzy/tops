# TitansOps - IT Operations Management Platform

![CI](https://github.com/infotitans/titansops/workflows/CI/badge.svg?branch=main)

TitansOps is an IT operations management platform developed by InfoTitans, designed to streamline and automate IT consulting operations. This application helps manage client projects, resources, and IT infrastructure monitoring.

**This app is using Flask 3.1.0 and Python 3.13.1**

## Tech stack

### Back-end

- [PostgreSQL](https://www.postgresql.org/) - For robust data storage
- [SQLAlchemy](https://github.com/sqlalchemy/sqlalchemy) - ORM for database operations
- [Redis](https://redis.io/) - For caching and task queue management
- [Celery](https://github.com/celery/celery) - For background task processing

### Front-end

- [esbuild](https://esbuild.github.io/) - For fast JavaScript bundling
- [TailwindCSS](https://tailwindcss.com/) - For utility-first CSS
- [Heroicons](https://heroicons.com/) - For consistent iconography
- [Hotwire Turbo + Stimulus](https://hotwired.dev/) - For dynamic interactions

## Key Features

- Client Project Management
- Resource Allocation
- IT Infrastructure Monitoring
- Automated Reporting
- SLA Tracking
- Asset Management
- Team Collaboration Tools

## Notable components and extensions

- **Packages and extensions**:
    - *[gunicorn](https://gunicorn.org/)* for production-grade application serving
    - *[Flask-DB](https://github.com/nickjj/flask-db)* for database management
    - *[Flask-Static-Digest](https://github.com/nickjj/flask-static-digest)* for static file optimization
    - *[Flask-Secrets](https://github.com/nickjj/flask-secrets)* for secure token management
    - *[Flask-DebugToolbar](https://github.com/flask-debugtoolbar/flask-debugtoolbar)* for development debugging

- **Quality Assurance**:
    - *[flake8](https://github.com/PyCQA/flake8)* for code linting
    - *[isort](https://github.com/PyCQA/isort)* for import organization
    - *[black](https://github.com/psf/black)* for code formatting
    - *[pytest](https://github.com/pytest-dev/pytest)* for comprehensive testing

## Running TitansOps

### Prerequisites

- Docker and Docker Compose v2
- On Windows, WSL2 is recommended for development

### Initial Setup

1. Clone the repository:
```sh
git clone https://github.com/infotitans/titansops
cd titansops
```

2. Configure environment:
```sh
cp .env.example .env
```

3. Build and start services:
```sh
docker compose up --build
```

4. Setup database:
```sh
./run flask db reset --with-testdb
```

### Development Commands

```sh
# Code quality checks
./run quality      # Run all quality checks
./run lint        # Lint code
./run format      # Format code
./run test        # Run tests

# Dependency management
./run deps:install  # Install/update dependencies
```

## Configuration

The application is configured through environment variables in the `.env` file. Key configurations include:

- Database credentials
- Redis settings
- Email configuration
- API keys
- Development/production mode switches

## Deployment

TitansOps supports deployment through Docker containers. Detailed deployment guides for various platforms are available in the `docs/deployment` directory.

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

## Support

For support, please contact the InfoTitans team at support@infotitans.com

## License

Copyright (c) 2025 InfoTitans. All rights reserved.

## About InfoTitans

InfoTitans is a leading IT consulting company specializing in enterprise IT solutions, digital transformation, and managed services. Visit [infotitans.com](https://infotitans.com) to learn more about our services.