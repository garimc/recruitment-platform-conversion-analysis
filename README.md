# Recruitment Platform Conversion Analysis - 신규 가입자 초기 행동 기반 전환 세그먼트 분석
![Image](https://github.com/user-attachments/assets/8dd0ee61-71cf-4256-abba-84d85780ea2f)
![Image](https://github.com/user-attachments/assets/c96f12bb-473a-40cb-954c-f2be969e2d85)
![Image](https://github.com/user-attachments/assets/c0f0acf4-ee5a-4b2a-9530-227340c5166f)

---

## TL; DR
- 신규 가입자는 감소세 → **전환 효율성** 제고가 핵심 과제  
- 최근 가입 유저일수록 **리텐션**이 높고, 전환 유저는 활동성·방문 리텐션·LTV가 더 높음  
- 초기 전환 예측 주요 변수: **평균 체류 시간**과 **총 페이지뷰 수**  
- 초기 행동 기반 5개 세그먼트: 빠르고 목표지향적(전환 100%) ↔ 낮은 활동성(전환 23%)

- New user sign-ups are declining, making **conversion efficiency** more critical.  
- More recent sign-ups show higher retention, and converted users have stronger **activity, visit retention, and LTV**.  
- Key predictors of early conversion: **average session time** and **total pageviews** (within first week).  
- Segmentation by early behavior reveals 5 user types, ranging from **fast & goal-oriented (100% conversion)** to **low-activity users (23% conversion)**.

---
## Project Overview
본 프로젝트는 채용 플랫폼 **신규 가입자의 초기 행동 데이터**를 기반으로 전환 효율성을 높이기 위한 요인을 탐색했습니다.  
**AARRR 프레임워크**, **예측 모델링**, **행동 기반 세그먼트 분석**을 통해 주요 지표(체류 시간, 페이지뷰)를 도출하고, 세그먼트별 맞춤 전략을 제안했습니다.

This project analyzes **early user behavior** on a recruitment platform to improve conversion efficiency.  
Using the **AARRR framework**, **predictive modeling** (Random Forest, Logistic Regression), and **behavior-based segmentation**, we identified key predictors (session time, pageviews) and derived tailored strategies by segment.

---

# Tech Stack
- Python (pandas, numpy, itertools, re)
- Visualization: matplotlib, seaborn
- Statistics: scipy, statsmodels
- Machine Learning: scikit-learn (RandomForest)
- Environment: Jupyter Notebook
  
---

## What's inside:
- 분석 통합 파일 Notebook (main) [`recruitment-platform-conversion-analysis.ipynb`](./recruitment-platform-conversion-analysis.ipynb)
- 프로젝트 보고서 파일 Full write-up: [`/reports/summary.md`](./reports/summary.md)
- 데이터 설명 Data dictionary: [`data/data_dictionary.md`](./data/data_dictionary.md)

---

## Project Structure
```
recruitment-platform-conversion-analysis/
├─ README.md
├─ recruitment-platform-conversion-analysis.ipynb
├─ reports/
│ └─ summary.md
├─ data/
│ └─ data_dictionary.md 
└─ requirements.txt
```

---

## Reproduce
1. 레포지토리 클론 (Clone this repository)
```
git clone https://github.com/garimc/recruitment-platform-conversion-analysis.git
cd recruitment-platform-conversion-analysis
```
2. 가상환경 생성 및 활성화 (선택) (Create a virtual environment (optional))
```
python -m venv .venv
source .venv/bin/activate
```
3. 필요한 패키지 설치 (Install dependencies)
```
pip install -r requirements.txt
```
4. 주피터 실행 (Run Jupyter Lab / Notebook)
```
jupyter lab
```
5. 노트북 열기 및 실행 (Open and run the notebook)
- [`recruitment-platform-conversion-analysis.ipynb`](./recruitment-platform-conversion-analysis.ipynb)
- 파일을 열고 위에서부터 차례대로 실행합니다.
- Execute all cells (top → bottom)

### ⚠️ 주의
- 코드와 분석 로직은 동일하게 실행할 수 있지만, 데이터가 없으므로 결과(숫자·그래프)는 재현되지 않습니다.
- Without the dataset, all analysis steps can be executed, but outputs (figures and numbers) cannot be reproduced.

---

## Data & Ethics
- 실제 데이터는 공유 불가 (보안 및 비밀유지 조항).
- 분석 과정, 코드, 변수 정의, 결과물만 공개.
- The original dataset cannot be shared due to security and confidentiality agreements.  
- Only the analysis process, code, variable definitions, and results are publicly available.

---

## Insights / Conclusions
1. **위기:** 신규 가입자는 감소세를 보이며, 유입 대비 전환(한 달 내 지원) 효율성 제고가 중요한 과제로 부상  
2. **기회:** 최근 가입한 유저일수록 지원 리텐션이 높으며, 전환 유저는 비전환 유저에 비해 활동성·방문 리텐션·LTV가 모두 높은 경향을 보임  
3. **모델링 결과:** 가입 후 일주일 내 평균 체류 시간(초), 총 페이지뷰 수가 주요 예측 변수로 도출됨  
4. **세그먼트 분석 및 전략:**  
가입 후 1주일 내 전환 여부, 평균 체류 시간 및 총 페이지뷰 수를 기준으로 유저를 분류한 결과, 다음과 같은 5개 세그먼트가 도출됨:  
- **세그먼트 1 – 빠르고 목표지향적 (1,484명, 전환률 1.00)**  
  → 개인화된 공고 추천으로 플랫폼 재방문 및 재지원 유도  

- **세그먼트 2 – 적극적이고 신중 (752명, 전환률 0.50)**  
  → FOMO 메시지로 지원 지연 방지 및 전환 촉진  

- **세그먼트 3 – 원하는 정보에 집중 (566명, 전환률 0.41)**  
  → 업종 맞춤 큐레이션 제공으로 탐색 시간 단축 및 빠른 전환 유도  

- **세그먼트 4 – 빠르고 다양한 정보 탐색 (214명, 전환률 0.33)**  
  → 명확한 기준 제시·심리적 부담 완화로 전환 장벽 해소  

- **세그먼트 5 – 낮은 활동성 (1,475명, 전환률 0.23)**  
  → 온보딩 미션 게임화·작은 성공 경험 설계로 초기 활동성 향상

1. **Crisis**: New user sign-ups are declining, making the improvement of conversion efficiency (within one month) a critical challenge.

2. **Opportunity**: Recent cohorts show higher application retention, and converted users exhibit stronger activity, revisit retention, and LTV compared to non-converted users.

3. **Modeling results**: Within the first week, average session time (sec) and total pageviews were identified as the key predictors of conversion.

4. **Segment analysis & strategies**:
Based on conversion status, average session time, and pageviews in the first week, users were divided into five segments:

- **Segment 1 – Fast & Goal-Oriented (1,484 users, 100% conversion)**
→ Encourage revisit and re-application through personalized job recommendations

- **Segment 2 – Proactive & Cautious (752 users, 50% conversion)**
→ Send FOMO-style nudges to prevent delays and accelerate conversion

- **Segment 3 – Focused Information Seekers (566 users, 41% conversion)**
→ Provide tailored curation by industry to shorten exploration time and drive faster conversion

- **Segment 4 – Rapid & Diverse Explorers (214 users, 33% conversion)**
→ Offer clear criteria and reduce psychological burden to lower conversion barriers

- **Segment 5 – Low-Activity Users (1,475 users, 23% conversion)**
→ Design gamified onboarding missions and small success experiences to boost early engagement
     
![Segment analysis graph](https://instinctive-milk-d9b.notion.site/image/attachment%3A6b25fe21-3ae4-411a-a7c4-82ca2aa9e2d6%3Aimage.png?table=block&id=2339d974-08e6-8072-bc0a-f3d8b83867ca&spaceId=f80357d3-0f5e-4223-be11-6f5365fc1458&width=1790&userId=&cache=v2)
*Figure 1. Segment-wise averages of key behavioral variables*

---

## License
- Code: MIT
- Reports & Figures: CC BY-NC 4.0
