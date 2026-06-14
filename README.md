# Word Memory Quiz

영단어를 사진이나 문서에서 추출하고, 뜻을 보고 영어 단어를 맞히는 방식으로 반복 학습할 수 있는 웹앱입니다.  
이미지 OCR뿐 아니라 PDF, Excel, Word, 텍스트 붙여넣기 입력도 지원하며, 추출된 단어를 바로 퀴즈로 연결할 수 있습니다.

전공영어 수업에서의 단어 외우기 과제를 더 효율적으로 수행하기 위해 제작했습니다.

## Live Demo

[GitHub Pages 바로가기](https://kyeoon.github.io/word-memory-quiz/)

## 주요 기능

- 이미지, PDF, Excel, Word, 텍스트 붙여넣기 입력 지원
- OCR 및 문서 텍스트 추출을 통한 `단어: 뜻` 형식 자동 분리
- `:` 앞부분을 단어로 인식하고, 괄호와 괄호 안 텍스트는 제거
- 뜻을 보고 영어 단어를 직접 입력하는 퀴즈 모드
- 띄어쓰기 차이와 한 글자 정도의 오타를 정답으로 허용
- 오타 허용 시 `오타:` 안내 문구 표시
- 인식된 단어 목록 확인, 발음 듣기, 불필요한 단어 삭제 기능
- 퀴즈 종료 후 점수 확인 및 재시험 보기 기능

## 사용 방법

1. 첫 화면에서 이미지 또는 문서를 업로드하거나 텍스트를 붙여넣습니다.
2. `단어 추출하기` 버튼을 눌러 단어와 뜻을 추출합니다.
3. 필요하면 `단어 확인하기`에서 목록을 검토하고, 잘못 인식된 단어를 삭제합니다.
4. `퀴즈 풀기`를 눌러 뜻을 보고 영어 단어를 입력합니다.
5. 퀴즈가 끝나면 점수를 확인하고 `재시험 보기`로 반복 학습할 수 있습니다.

## 권장 입력 형식

가장 안정적인 형식은 아래처럼 한 줄에 하나씩 `단어: 뜻` 형태로 정리하는 것입니다.

```text
abandon: give up completely
ability: the power to do something
benefit (n): advantage or profit
```

위 예시에서는 `benefit (n)`처럼 괄호가 있어도 실제 단어는 `benefit`으로 저장됩니다.

## 지원 파일 형식

- 이미지: `png`, `jpg`, `jpeg`, `webp`, `bmp`
- 문서: `pdf`, `xlsx`, `xls`, `csv`, `docx`
- 붙여넣기 입력: `단어: 뜻` 형식 텍스트

`doc` 형식은 브라우저에서 정확한 추출이 어려워 `docx`로 변환 후 업로드하는 것을 권장합니다.

## 기술 스택

- HTML
- CSS
- Vanilla JavaScript
- [Tesseract.js](https://github.com/naptha/tesseract.js) for OCR
- [PDF.js](https://mozilla.github.io/pdf.js/) for PDF parsing
- [SheetJS](https://sheetjs.com/) for Excel parsing
- [Mammoth.js](https://github.com/mwilliamson/mammoth.js) for Word parsing
- Web Speech API for pronunciation
- GitHub Pages for deployment

## OCR 정확도 안내

OCR 성능은 원본 품질의 영향을 많이 받습니다. 정확도를 높이려면 아래 방법을 추천합니다.

- 흐릿하지 않고 대비가 높은 이미지 사용
- 기울어지지 않은 정면 캡처 사용
- 텍스트 기반 PDF, Excel, Word 파일 우선 사용
- 가능하면 `단어: 뜻` 구조가 명확한 자료 사용

스캔 이미지보다 텍스트가 실제로 포함된 PDF나 문서 파일이 훨씬 더 정확하게 추출됩니다.

## 배포

이 프로젝트는 GitHub Pages로 배포되어 있으며, 정적 웹앱 형태로 별도 서버 없이 실행됩니다.

## License

This project is for educational and personal learning use.
