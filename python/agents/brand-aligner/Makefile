.PHONY: help install run format lint check test

help:
	@echo "Available commands for Brand Aligner Agent:"
	@echo "  make install  - Install dependencies using uv"
	@echo "  make run      - Run the agent's web UI"
	@echo "  make format   - Format code using ruff"
	@echo "  make lint     - Lint code using ruff"
	@echo "  make check    - Run linting and formatting checks"
	@echo "  make test     - Run unit tests using pytest"
	@echo "  make deploy   - Deploy the agent to Agent Engine"

install:
	uv pip install -e .[dev]

run:
	uv run adk web --log_level DEBUG

format:
	uv run ruff format .

lint:
	uv run ruff check .

check:
	uv run ruff check .
	uv run ruff format --check .

test:
	uv run pytest -v

deploy:
	uv run deployment/deploy.py
