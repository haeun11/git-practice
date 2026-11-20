
배포 URL: https://haeun11.github.io/git-practice/
# Git practice

name : Haeun Kim
number : 32237248

## OrderLab (Python CI/CD 실습)

Ruff · pytest · GitHub Actions 로 계산 → 검증 → CSV → API → 배포까지 확장한 실습 프로젝트

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\Activate.ps1
python -m pip install -r requirements-dev.txt

ruff check .
ruff format --check .
python -m pytest -q
python -m pytest --cov=orderlab --cov-report=term-missing
python generate_report.py        # site/index.html 생성
```

- `.github/workflows/ci.yml` : Push/PR 마다 lint job + OS별(ubuntu, windows) test job, coverage.xml artifact 업로드
- `.github/workflows/ci-cd.yml` : PR 은 quality 만, main Push 는 quality 통과 후 GitHub Pages 배포

배포 URL: https://haeun11.github.io/git-practice/
