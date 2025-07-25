# Project Name - Claude Assistant Notes

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

Brief description of what this project does and its main purpose.

## Architecture & Key Components

### Project Structure
```
project-root/
├── src/           # Source code
├── tests/         # Test files
├── docs/          # Documentation
└── scripts/       # Build and utility scripts
```

### Core Technologies
- **Language**: [Primary language and version]
- **Framework**: [Main framework if applicable]
- **Database**: [Database system if applicable]
- **Key Dependencies**: [List major dependencies]

## Common Commands

### Setup and Installation
```bash
# Clone and install dependencies
git clone <repository-url>
cd <project-name>
npm install  # or appropriate package manager

# Setup environment variables
cp .env.example .env
# Edit .env with your values
```

### Development
```bash
# Start development server
npm run dev

# Run tests
npm test

# Run tests in watch mode
npm run test:watch

# Lint code
npm run lint

# Format code
npm run format
```

### Build and Deploy
```bash
# Build for production
npm run build

# Run production build locally
npm run preview

# Deploy (update with actual deployment command)
npm run deploy
```

## Development Guidelines

### Code Style
- Follow [ESLint/Prettier/other] configuration
- Use consistent naming conventions:
  - Files: `kebab-case.js`
  - Components/Classes: `PascalCase`
  - Functions/Variables: `camelCase`
  - Constants: `UPPER_SNAKE_CASE`

### Git Workflow
- Branch naming: `feature/description`, `fix/issue-description`
- Commit messages: Use conventional commits (feat:, fix:, docs:, etc.)
- Always create PR for code review

### Testing Strategy
- Write tests for new features
- Maintain test coverage above X%
- Run tests before committing

## Common Issues and Solutions

### Issue: [Common problem #1]
**Symptoms**: Description of what goes wrong
**Solution**: 
```bash
# Commands or steps to fix
```

### Issue: [Common problem #2]
**Symptoms**: Description of what goes wrong
**Solution**: 
```bash
# Commands or steps to fix
```

## Project-Specific Patterns

### API Endpoints
- Base URL: `/api/v1`
- Authentication: Bearer token in headers
- Standard response format:
```json
{
  "success": boolean,
  "data": object | array,
  "error": string | null
}
```

### Database Queries
- Use prepared statements
- Connection pooling is configured in `db/config.js`
- Migrations located in `db/migrations/`

### Error Handling
- All errors should be caught and logged
- Use custom error classes from `src/errors/`
- Return appropriate HTTP status codes

## Environment Variables

Required environment variables:
```bash
NODE_ENV=development|production
PORT=3000
DATABASE_URL=postgresql://...
API_KEY=your-api-key
# Add other required vars
```

## Debugging Tips

### Enable Debug Logging
```bash
DEBUG=app:* npm run dev
```

### Common Debug Commands
```bash
# Check running processes
ps aux | grep node

# View logs
tail -f logs/app.log

# Database debugging
npm run db:console
```

## Performance Considerations

- Keep bundle size under X MB
- Lazy load heavy components
- Use caching where appropriate
- Database queries should use indexes

## Security Guidelines

- Never commit secrets or API keys
- Validate all user input
- Use parameterized queries
- Keep dependencies updated
- Follow OWASP guidelines

## Additional Resources

- [Link to detailed documentation]
- [Link to API documentation]
- [Link to architecture diagrams]
- [Link to team conventions guide]

## Notes

- This file should be updated as the project evolves
- When adding new patterns or solving new issues, document them here
- Keep information concise and actionable for Claude