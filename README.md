# 🧠 PubMedQA 한국어 T5 파인튜닝 프로젝트

### 🔍 프로젝트 개요
이 프로젝트는 **PubMedQA-test-Ko 데이터셋**을 이용하여  
의학 질문(Question)에 대한 **전문가 수준의 소견(Answer)** 을  
생성하는 **한국어 T5 모델(`paust/pko-t5-small`) 파인튜닝 프로젝트**입니다.

---

### 🧩 모델 구성

| 항목 | 내용 |
|------|------|
| **기반 모델** | [paust/pko-t5-small](https://huggingface.co/paust/pko-t5-small) |
| **데이터셋** | [ChuGyouk/PubMedQA-test-Ko](https://huggingface.co/datasets/ChuGyouk/PubMedQA-test-Ko) |
| **프레임워크** | Hugging Face Transformers, Datasets |
| **환경** | Python 3.10 / Google Colab / CUDA (T4 GPU) |
| **학습 목적** | 한국어 의학 질의응답(QA) 모델 생성 |

---

### ⚙️ 데이터 구조
데이터는 **의학 질문(QUESTION)** 과 **긴 소견(LONG_ANSWER)** 으로 구성됩니다.

| 컬럼명 | 설명 |
|--------|------|
| `QUESTION` | 의학 관련 질문 텍스트 |
| `LONG_ANSWER` | 질문에 대한 논문 기반의 정답 텍스트 |

> 예시:
> ```
> QUESTION: 비만은 심혈관 질환의 주요 위험 요인인가요?
> LONG_ANSWER: 비만은 고혈압, 당뇨병, 이상지질혈증을 유발하며, 심혈관 질환의 주요 위험 요인으로 간주된다.
> ```

---

### 🧑‍💻 실행 방법

#### 1️⃣ 환경 설정
```bash
!pip install -U transformers datasets accelerate
