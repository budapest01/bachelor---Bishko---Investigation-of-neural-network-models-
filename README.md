
# Solar PV Forecast API

Цей проєкт реалізує нейромережеву модель для прогнозування генерації сонячної електроенергії на основі погодинних метеоданих та історичних показників виробітку. Модель розгорнута у вигляді Flask API та контейнеризована за допомогою Docker.

## 📦 Структура проєкту

- `app.py` — основний серверний файл Flask API
- `solar_pv_forecast_colab.ipynb` — Jupyter Notebook з реалізацією моделі
- `Dockerfile` — інструкції для створення Docker-контейнера
- `requirements.txt` — список Python-залежностей
- `docker-compose.yml` — зручний запуск сервісу через Docker Compose

## 🚀 Запуск у Docker

1. Скопіюйте всі файли в один проєкт
2. Побудуйте контейнер і запустіть:

```bash
docker-compose up --build
```

3. API буде доступне на `http://localhost:5000`

## 🔄 Приклад використання API

```bash
curl -X POST http://localhost:5000/predict \
     -H "Content-Type: application/json" \
     -d '{"temperature": 23.5, "cloudcover": 0.3, "radiation": 650.0}'
```

## 🧠 Моделі

У проєкті реалізовано моделі на основі глибокого навчання, включаючи MLP, GRU, LSTM, CNN та їх комбінації. Найвищу точність показала архітектура CNN+LSTM.

## 📈 Бібліотеки

- TensorFlow
- Flask
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

## 👨‍💻 Автор

Бішко Віталій, ІТ СТЕП Університет, 2025
