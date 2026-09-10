# Google Colab 시작하기

## 1분 요약 흐름

1. `colab.new`로 새 노트북을 연다. ([colab.google](https://colab.google/))
2. 제목(파일명)을 바꾸고, 셀에 코드를 적은 뒤 **Shift + Enter**로 실행한다.
3. 작업은 자동으로 Google Drive에 저장되지만(노트북 파일), **/content에 만든 파일은 세션이 끝나면 사라질 수 있어** Drive에 저장/마운트한다. ([research.google.com](https://research.google.com/colaboratory/faq.html))
4. 필요하면 **Runtime → Change runtime type**에서 GPU/TPU를 켠다. ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

## Colab이 뭐예요?

- **Google Colab(Colaboratory)**은 브라우저에서 바로 쓰는 “클라우드 주피터 노트북”이에요. 설치 없이 시작할 수 있고, 상황에 따라 GPU/TPU 같은 연산 자원도 쓸 수 있어요. ([colab.google](https://colab.google/))
- 문서(설명/메모)와 코드(파이썬 실행)가 한 화면에 섞여 있는 형태라서, **공부/실험/과제**에 특히 편합니다.

------

## 준비물 (딱 3개)

- Google 계정 (Gmail 계정)
- 크롬(Chrome) 같은 최신 브라우저
- 인터넷

------

## 핵심 용어만 먼저 잡고 가기

- **노트북(Notebook)**: `.ipynb` 형식의 파일(설명+코드+결과가 함께 저장됨). ([research.google.com](https://research.google.com/colaboratory/faq.html))
- **셀(Cell)**: 노트북 안의 한 “블록”.
  - **코드 셀**: 파이썬을 실행하는 칸
  - **텍스트(마크다운) 셀**: 설명/메모를 적는 칸
- **런타임(Runtime)**: 코드를 실제로 돌려주는 “가상 컴퓨터(서버)”.
  - 일정 시간 놀리면 종료되거나(Idle timeout), 최대 실행 시간이 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
  - 런타임은 “임시”라서, 런타임 안(/content)에 만든 파일은 세션이 끝나면 사라질 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

## Colab 여는 방법 3가지 (쉬운 순)

### 방법 A) 가장 빠른 시작: 새 노트북 바로 열기

1. 브라우저 주소창에 `colab.new` 입력
2. 새 노트북이 열리면 바로 시작! ([colab.google](https://colab.google/))

### 방법 B) Google Drive에서 만들기 (파일 정리하기 편함)

1. Google Drive 열기
2. **새로 만들기(New) → 더보기(More) → Colaboratory** 선택 ([Google for Developers](https://developers.google.com/earth-engine/guides/python_install-colab))
3. 지금 있는 폴더에 노트북이 만들어져서 관리가 편해요.

### 방법 C) Colab 화면에서 만들기

1. Colab 사이트로 들어가기 (검색창에 “Google Colab” 검색)
2. 메뉴에서 **File → New → New Python 3 notebook** ([Google for Developers](https://developers.google.com/earth-engine/guides/python_install-colab))

------

## 처음 열면 꼭 해야 하는 2가지

### 1) 노트북 이름(제목) 바꾸기

- 상단의 “Untitled…” 같은 제목을 클릭 → 원하는 이름 입력
- 이름을 잘 붙이면 Drive에서 찾기 쉬워요.

### 2) 내 노트북이 Drive 어디에 저장되는지 감 잡기

- Colab에서 만든 노트북은 기본적으로 Drive의 **‘Colab Notebooks’ 폴더**에 저장되는 경우가 많아요. ([Google for Developers](https://developers.google.com/earth-engine/guides/python_install-colab))
- 노트북을 찾을 때는:
  - Drive에서 검색하거나
  - Colab에서 **File → Open notebook**로 최근/Drive/GitHub 등에서 열 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

## 첫 실행: “Hello, Python!” (진짜 30초)

1. 노트북이 열리면 빈 코드 셀이 보입니다.
2. 아래를 그대로 입력:

```python
print("Hello, Colab!")
```

1. **Shift + Enter**를 누릅니다.
2. 아래에 `Hello, Colab!`가 출력되면 성공!

추가로 이것도 해보세요:

```python
2 + 3 * 10
```

------

## “저장”을 제대로 이해하는 것이 Colab의 절반입니다

### 노트북(.ipynb)은 Drive에 저장됨

- Colab 노트북은 **Google Drive에 저장**되고, 형식은 **Jupyter 노트북(.ipynb)**입니다. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 공유도 Google Docs처럼 **오른쪽 위 Share 버튼**으로 할 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))

### 하지만 런타임(가상 컴퓨터)은 임시일 수 있음

- Colab 코드는 내 계정 전용 가상 머신에서 실행되지만,
  **한동안 사용하지 않으면 삭제되거나 최대 수명이 있어** 실행 상태가 초기화될 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))

#### 딱 한 줄 결론

- **“노트북 파일”은 Drive에 남는다.**
- **“/content에 만든 파일/설치한 것”은 런타임이 끝나면 사라질 수 있다.**

아래 표로 보면 더 직관적이에요:

| 구분               | 어디에 있음  | 세션 종료 후   | 예시                              |
| ------------------ | ------------ | -------------- | --------------------------------- |
| 노트북(.ipynb)     | Google Drive | 남음           | 코드/설명/출력                    |
| 런타임 파일        | `/content`   | 사라질 수 있음 | 다운로드한 데이터, 생성한 이미지  |
| 런타임 패키지 설치 | 런타임 내부  | 사라질 수 있음 | `pip install`로 설치한 라이브러리 |

------

## Google Drive 파일을 Colab에서 쓰는 가장 흔한 방법 (중요)

### 1) Drive 마운트(연결)하기

아래 코드를 실행하면 Drive를 Colab 런타임에 연결할 수 있어요.

```python
from google.colab import drive
drive.mount('/content/drive')
```

- 연결되면 보통 내 Drive가 이런 경로로 보입니다:
  - `/content/drive/MyDrive/` (내 드라이브)

### 2) Drive에 파일 저장/불러오기 예시

```python
import pandas as pd

path = "/content/drive/MyDrive/sample.csv"
df = pd.read_csv(path)
df.head()
```

### 자주 나는 오류: “drive.mount timed out”

- Drive 마운트가 “timeout” 되는 경우가 있는데, Colab FAQ에서는 **My Drive 루트에 파일/폴더가 너무 많으면 문제가 생길 수 있다**고 안내합니다. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 해결 팁: Drive의 최상단(루트)에 파일을 너무 많이 쌓지 말고 폴더로 정리하기.

------

## 런타임(Runtime) 다루기: CPU/GPU/TPU 켜는 법까지

### 런타임 바꾸기 (GPU/TPU 켜기)

1. 상단 메뉴에서 **Runtime → Change runtime type**
2. **Hardware accelerator**에서 CPU/GPU/TPU 선택 ([research.google.com](https://research.google.com/colaboratory/faq.html))

> 참고: GPU 런타임을 켰다고 해서 자동으로 GPU를 “사용”하는 건 아니고, GPU를 실제로 쓰는 코드여야 GPU가 활용됩니다. ([research.google.com](https://research.google.com/colaboratory/faq.html))

### 무료 사용 시 알아둘 점 (중요)

- Colab은 사용량 제한이 있고, **유휴 시간(Idle) 타임아웃**, **최대 실행 시간**, **사용 가능한 GPU/TPU 종류** 등이 변동될 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 무료 버전은 상황에 따라 **최대 12시간 정도** 실행될 수 있다고 안내되어 있어요(조건/사용 패턴에 따라 달라질 수 있음). ([research.google.com](https://research.google.com/colaboratory/faq.html))

### “환경이 바뀌어서 코드가 깨져요”를 줄이는 팁: 런타임 버전 고정

- Colab은 런타임이 “동적”이라 패키지 버전이 바뀌어 결과가 달라질 수 있는데,
  2025년에는 **Change runtime type 대화상자에 Runtime Version Selector(버전 선택)** 기능이 추가되어 특정 런타임 버전으로 “핀(pin)”할 수 있다고 소개됐습니다. ([Google Developers Blog](https://developers.googleblog.com/google-colab-adds-more-back-to-school-improvements/))
- 수업/과제/프로젝트처럼 “언제 돌려도 똑같이 돌아가야 하는” 상황이면 도움이 돼요.

### 런타임 초기화(문제 생길 때)

- 런타임이 꼬였거나 이상하면 **Runtime → Disconnect and delete runtime**으로 초기 상태로 되돌릴 수 있어요(자주 못 하게 제한이 있을 수 있음). ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

## 패키지 설치(예: pandas, numpy 등) 기본

Colab은 대부분 기본 라이브러리가 있지만, 없으면 이렇게 설치합니다:

```python
!pip install pandas
```

- 느낌표 `!`는 “리눅스 명령어를 실행”한다는 뜻이에요.
- 런타임이 초기화되면 다시 설치해야 할 수도 있으니, 보통 노트북 맨 위에 “설치 셀”을 만들어 둡니다. ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

## 기존 .ipynb 노트북 가져오기 (파일이 이미 있을 때)

- Colab에서 **File 메뉴 → “Upload notebook”**으로 기존 Jupyter/Colab 노트북을 올려서 열 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 또는 Drive에 `.ipynb`를 올려서 “연결 앱(Colaboratory)”로 열 수도 있어요. ([Google for Developers](https://developers.google.com/earth-engine/guides/python_install-colab))

------

## 초보자가 자주 겪는 문제 TOP 5 (해결 바로 적어둠)

### 1) “어제 만든 파일이 없어졌어요”

- `/content`에 저장했다면 런타임 종료로 날아갈 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 해결: Drive 마운트 후 `/content/drive/MyDrive/...`에 저장

### 2) “ModuleNotFoundError: No module named …”

- 필요한 패키지가 설치되어 있지 않음
- 해결: `!pip install 패키지명` 실행

### 3) “런타임이 끊겼어요 / 다시 연결하래요”

- Colab은 유휴 시간이 길면 끊길 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 해결: 재연결 후 “위에서부터 셀 실행” (환경을 다시 만드는 게 핵심)

### 4) “GPU 켰는데 느려요”

- GPU를 쓰는 코드가 아니거나, 데이터/전처리가 병목일 수 있어요. ([research.google.com](https://research.google.com/colaboratory/faq.html))
- 해결: 정말 GPU 연산(딥러닝 등)을 하고 있는지 점검

### 5) “내 노트북이 어디 갔는지 모르겠어요”

- Drive 검색 또는 Colab의 **File → Open notebook** 이용 ([research.google.com](https://research.google.com/colaboratory/faq.html))
- Colab에서 만든 건 기본적으로 Drive의 **Colab Notebooks**에 있을 가능성이 큼 ([Google for Developers](https://developers.google.com/earth-engine/guides/python_install-colab))

------

## (선택) Colab을 더 쉽게 쓰는 습관 3가지

1. **맨 위 셀에 “환경 준비 셀” 만들기**
   - Drive 마운트, 패키지 설치, 데이터 경로 등을 한 곳에 모아두기
2. **텍스트(마크다운) 셀로 설명을 꼭 같이 적기**
   - 나중에 다시 봐도 이해가 쉬움
3. **작업 결과(모델/데이터/이미지)는 Drive에 저장**
   - 런타임이 끊겨도 결과물이 남음 ([research.google.com](https://research.google.com/colaboratory/faq.html))

------

