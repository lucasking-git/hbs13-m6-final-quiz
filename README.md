# HBS 13기 6모듈 재무 Final Test 연습 퀴즈

HBS 6모듈 재무 시험 Final Test를 연습할 수 있는 정적 웹 앱입니다.

- 총 25문제 예정: 객관식 20문제(4지선다) + 주관식 5문제
- 입장 비밀번호로 접근 제한 (개인 학습용 단순 잠금)
- 문제 순서 / 보기 순서 무작위 옵션
- 문제별 즉시 채점 + 교수님 해설 표시
- 결과 요약 및 틀린 문제만 다시 풀기

## 배포

GitHub Actions(`.github/workflows/deploy.yml`)가 푸시 시 사이트 파일을 `gh-pages` 브랜치로 발행하고, GitHub Pages가 그 브랜치를 서빙합니다.

배포 주소: `https://lucasking-git.github.io/hbs13-m6-final-quiz/`

## 문제 추가 방법

`questions.js` 의 `QUIZ_QUESTIONS` 배열에 항목을 추가하면 됩니다. 형식은 파일 상단 주석을 참고하세요.

- 객관식: `type: "mc"`, `choices` 4개, `answer`는 0부터 시작하는 정답 인덱스(①=0)
- 주관식: `type: "short"`, `answers`에 정답 키워드 배열, `model`에 모범 답안

로비 화면에 1~25번 슬롯이 표시되며, 확인된 문제만 초록색으로 표시됩니다.

## 로컬 실행

정적 파일이므로 `index.html`을 브라우저로 열거나 간단한 서버로 실행하면 됩니다.

```bash
python3 -m http.server 8080
```
