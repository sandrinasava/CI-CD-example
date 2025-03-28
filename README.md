# CI/CD Workflows
### Описание
В этом репозитории настроены GitHub Actions для автоматизации процессов сборки, тестирования и линтинга кода. Вот описание каждого из workflows:
### 1. Workflow для ветки master
- **Файл:** .github/workflows/go.yml
- **Триггер:** Запускается при push в ветку master
- **Задачи:**
   - **Build:** Сборка всех пакетов   ```
                                     go build -v ./...
                                     ```
   - **Tests:** Запуск тестов ```
                                     go test -v ./...
                                     ```
  - **Tests (Race):** Проверка состояния гонки ```bash
                                     go test -race -v ./...
                                     ```
  - **Lint:** Проверка на соответствие стилю с помощью действия  ```
                                     golangci-lint
                                     ```
### 2. Workflow для ветки new_workflow
- **Файл:** .github/workflows/go2.yml
- **Задачи:**
   - **Build:** Сборка всех пакетов   ```
                                     go build -v ./...
                                     ```
   - **Tests:** Запуск тестов ```
                                     go test -v ./...
                                     ```
