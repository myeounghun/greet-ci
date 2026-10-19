# greet-ci

인사말 프로그램의 GitHub Actions CI 구성 실습입니다.

## 요구사항

- Python >= 3.11
- uv

## 실행 방법

인수 없이 실행:
```bash
uv run --locked python greet.py
```
출력:
```text
Hello, world!
```

이름 인수 전달 실행:
```bash
uv run --locked python greet.py Hee
```
출력:
```text
Hello, Hee!
```

## 검사 및 테스트

테스트 실행:
```bash
uv run --locked pytest -q greet.py
```

코드 포맷 검사:
```bash
uv run --locked black --check greet.py
```

린트 검사:
```bash
uv run --locked flake8 greet.py
```

타입 검사:
```bash
uv run --locked mypy greet.py
```

패키지 빌드:
```bash
uv build
```