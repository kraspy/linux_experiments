FROM astral/uv:python3.12-alpine

LABEL maintainer="kraspy@yandex.ru"

ENV PYTHONUNBUFFERED=1
ENV PATH="/app/.venv/bin:$PATH"
ENV SQLALCHEMY_PG_CONN_URI="postgresql+asyncpg://kraspy:password@db/main_db"

WORKDIR /app

COPY . .

RUN uv sync

CMD ["python", "main.py"]