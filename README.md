FastAPI application to generate summarized web pages using Newspaper3k using a TDD approach using pytext with code coverage (pytest-cov) and code quality (flake8) checks
# Application Docker Setup

## Build and Run

1. **Build the Docker image:**

   ```bash
   docker-compose build
   ```

2. **Start the application in detached mode:**
    ```bash
    docker-compose up -d
    ```

3. **Open your browser and navigate to http://localhost:8004/docs**

## Other interesting commands
1. **To execute tests**
    ```bash
    docker-compose exec web python -m pytest -p no:warnings
    ```

2. **To execute coverage**
    ```bash
    docker-compose exec web python -m pytest --cov="."
    ```

3. **To execute code quality check**
    ```bash
    docker-compose exec web flake8 .
    ```

4. **To execute code black check**
    ```bash
    docker-compose exec web black . --check
    ```

5. **To generate schemas for db**
    ```bash
    docker-compose exec web python app/db.py
    ```

6. **To apply migrations to db**
    ```bash
    docker-compose exec web aerich upgrade
    ```