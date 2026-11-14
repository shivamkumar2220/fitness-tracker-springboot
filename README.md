# Fitness Tracker (Spring Boot)

A web app for tracking workouts and fitness progress, with separate dashboards for admins and users.

## The problem

Most beginners log workouts in notes or spreadsheets, which makes it hard to see progress over time or stay motivated. This app keeps workouts, progress and challenges in one place, and gives admins a dashboard to manage users and content.

## Features

**User dashboard**
- Log workouts
- See progress insights as charts
- Join fitness challenges
- Read curated guidance content

**Admin dashboard**
- Manage users
- Approve community content
- Configure system settings
- Monitor engagement metrics

## Tech stack

| Layer | Technology |
|---|---|
| Language | Java 17 |
| Framework | Spring Boot 3.3 (Spring MVC) |
| Persistence | Spring Data JPA, H2 in-memory database |
| UI | Thymeleaf templates, CSS, Chart.js |
| Build and tests | Maven, JUnit |

## Getting started

Requirements: JDK 17+ and Maven.

```bash
git clone https://github.com/shivamkumar2220/fitness-tracker-springboot.git
cd "fitness-tracker-springboot/FITNESS TRACKING APP"
mvn spring-boot:run
```

Then open:

- Admin dashboard: http://localhost:8080/admin (demo login `admin@example.com` / `admin123`, seeded locally on startup)
- Sample user dashboard: http://localhost:8080/user?userId=2

The H2 database is in-memory, so data resets on every restart. To use MySQL or PostgreSQL instead, change the `spring.datasource.*` settings in `application.yml`.

## Running tests

```bash
mvn test
```

The tests cover application startup and the `UserService` workout logging and analytics.

## Project structure

```
FITNESS TRACKING APP/
├── pom.xml
└── src/
    ├── main/java/com/sach/fitnesstracker/
    │   ├── config/       # Seeds demo data on startup
    │   ├── controller/   # Admin and user MVC controllers
    │   ├── dto/          # Dashboard view models
    │   ├── model/        # JPA entities
    │   ├── repository/   # Spring Data repositories
    │   └── service/      # Business logic
    ├── main/resources/
    │   ├── templates/    # Thymeleaf views
    │   └── static/       # CSS and Chart.js scripts
    └── test/             # Unit tests
```

## Screenshots

_Add screenshots of the admin and user dashboards here._

## Planned improvements

- Switch to a persistent database and add proper authentication
- Expose REST APIs for a mobile client
- Goal tracking and notifications

## License

MIT
