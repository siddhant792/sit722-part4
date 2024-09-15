FROM python:3.9-slim

WORKDIR /app/inventory_management

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV PYTHONUNBUFFERED=1
ENV DATABASE_URL=postgresql://task_8_2_p_user:l59R7LSn5jvbSo8r7RxGOoerogyVujhT@dpg-crgjdbqj1k6c739ih7o0-a.oregon-postgres.render.com/task_8_2_p

EXPOSE 8001

CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8001"]
