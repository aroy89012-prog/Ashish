# Backend Security Checklist

## Node.js Express
- **Input Validation**: Always validate and sanitize user inputs to prevent malicious data.
- **SQL Injection Prevention**: Use parameterized queries and ORM tools to protect against SQL injection.
- **Authentication**: Implement secure authentication strategies, such as JWT (JSON Web Tokens) or OAuth.
- **CORS**: Configure Cross-Origin Resource Sharing to allow trusted domains only (e.g., `app.use(cors({ origin: 'https://yourtrusteddomain.com' }))`).
- **Rate Limiting**: Use libraries like `express-rate-limit` to limit repeated requests to public APIs.
- **Error Handling**: Implement centralized error handling to avoid leaking sensitive information.
- **Logging**: Ensure proper logging of application events and errors using libraries like `morgan`.
- **Secrets Management**: Store sensitive information such as API keys and passwords securely using environment variables or secret management tools.

## Python Django/Flask
- **Input Validation**: Ensure to validate and sanitize inputs using Django forms or Flask-WTF.
- **SQL Injection Prevention**: Use Django ORM or SQLAlchemy for database interactions to avoid SQL injection.
- **Authentication**: Utilize Django's built-in authentication or Flask-Security for secure user management.
- **CORS**: Configure CORS in Django or Flask to allow only trusted origins.
- **Rate Limiting**: Implement rate limiting using Django Ratelimit or Flask-Limiter.
- **Error Handling**: Use custom error handlers to manage exceptions and avoid revealing sensitive data.
- **Logging**: Use Django's logging framework or Flask-Logging to capture logs properly.
- **Secrets Management**: Use `django-environ` or environment variables in Flask for managing secrets.

## Java Spring Boot
- **Input Validation**: Utilize Java Bean Validation (JSR-380) to validate inputs.
- **SQL Injection Prevention**: Use Spring Data JPA or Hibernate to avoid SQL injection vulnerabilities.
- **Authentication**: Implement Spring Security for robust authentication and authorization.
- **CORS**: Configure CORS in Spring Boot by using `@CrossOrigin` annotation or global configuration.
- **Rate Limiting**: Use Spring Cloud Gateway or other middleware for rate limiting APIs.
- **Error Handling**: Implement global exception handling using `@ControllerAdvice`.
- **Logging**: Leverage SLF4J with Logback or Log4j for effective logging.
- **Secrets Management**: Use Spring Cloud Config or other libraries for managing secrets securely.