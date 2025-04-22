
# Мульти-агентная система с интеграцией OpenRouter

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Система с интеллектуальными агентами для обработки различных типов запросов с использованием API OpenRouter и внешних сервисов.

## 🌟 Особенности

- 🕸️ Поддержка мульти-агентной архитектуры
- 🤖 Интеграция с OpenAI через OpenRouter
- 🌦️ Получение данных о погоде (OpenWeatherMap)
- 💹 Парсинг курсов валют (ЦБ РФ)
- 📰 Анализ новостной ленты (RSS ЦБ РФ)
- 🧠 Интеллектуальный роутинг запросов
- ⚡ Потоковая обработка ответов

## 🛠️ Установка

1. Клонировать репозиторий:
```bash
git clone https://github.com/artystyle/hse_llm_examples
cd hse_llm_examples
```

2. Создать и активировать виртуальное окружение:
```bash
python -m venv venv
source venv/bin/activate  # Linux/MacOS
venv\Scripts\activate  # Windows
```

3. Установить зависимости:
```bash
pip install -r requirements.txt
```

## ⚙️ Настройка

1. Получить API-ключи:
- [OpenRouter](https://openrouter.ai/keys)
- [OpenWeatherMap](https://openweathermap.org/api)

2. Создать файл `hse.env` в корне проекта:
```hse.env
OPENROUTER_API_KEY=your_openrouter_key
WEATHERMAP_API_KEY=your_weather_api_key
```

## 🚀 Использование

Запуск системы:
```python
python main.py
```

Примеры запросов:
```python
"Какая погода в Москве и текущий курс доллара?"
"Последние новости ЦБ и курс евро"
"Что нового в экономической политике?"
```

## 🧩 Компоненты системы

### Агенты
- **WeatherAgent**: Получение данных о погоде
- **FinanceAgent**: Парсинг курсов валют
- **NewsAgent**: Анализ новостной ленты ЦБ

### Пример кода
```python
class NewsAgent(Agent):
    def get_news(self, count=3, keywords=None):
        # Реализация парсинга RSS
        # Возвращает структурированные данные
```

## 📊 Пример вывода
```json
{
  "weather": {
    "location": "Москва",
    "temp": 18.5,
    "humidity": 65
  },
  "finance": {
    "USD": 75.3,
    "EUR": 89.7
  }
}
```

## 📦 Зависимости
- `openai >= 1.0.0`
- `requests >= 2.31.0`
- `feedparser >= 6.0.10`
- `python-dotenv >= 1.0.0`
- `pytz >= 2023.3`

## 📄 Лицензия
Этот проект распространяется под лицензией MIT. Подробности см. в файле [LICENSE](LICENSE).

```

Этот README включает все основные разделы для быстрого старта с проектом. Для реального использования нужно:
1. Заменить `yourusername` на актуальную ссылку репозитория
2. Добавить реальное содержимое файла `requirements.txt`
3. При необходимости дополнить документацию
4. Добавить скриншоты работы системы
