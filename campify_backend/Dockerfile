# Используем официальный образ Python из Docker Hub
FROM python:3.10

# Устанавливаем рабочую директорию в контейнере
WORKDIR /campify_backend

# Копируем файлы requirements.txt и entrypoint.sh в контейнер
COPY requirements.txt /campify_backend/

RUN pip install --upgrade pip


# Устанавливаем зависимости
RUN pip install -r requirements.txt

# Копируем остальные файлы проекта в контейнер
COPY . .

# Устанавливаем переменные окружения
ENV PYTHONUNBUFFERED=1

# Открываем порт, на котором будет работать приложение
EXPOSE 8000
