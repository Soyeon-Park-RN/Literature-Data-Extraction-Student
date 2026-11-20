# Literature Data Extraction (Student) — Claude Skill
![For Students](https://img.shields.io/badge/For-Students-5B8DEF.svg)

체계적 문헌고찰의 데이터 추출을 Claude와 함께 연습하는 학생용 스킬입니다. 논문 PDF를 올리면 "이 논문은 어떤 설계인가 → 무엇을 뽑아야 하는가 → 값은 얼마인가" 순서로 질문이 하나씩 나타납니다. 항목마다 논문의 어디를 보면 되는지, 어떤 점을 헷갈리기 쉬운지 안내가 붙어 있으니 그걸 참고해 먼저 적으세요. 그다음 Claude가 따로 뽑은 값과 비교합니다. 값이 다르면 왜 다른지 — 이 항목을 왜 뽑는지, 논문의 어느 문장이 근거인지, 왜 그 값인지 — 자세히 설명해 줍니다. 덜 적었을 뿐 틀리지 않았으면 "이것도 덧붙이면 좋겠다"고 제안만 합니다. 최종 결정은 언제나 여러분이 합니다. 결과는 추출표와 학습 기록이 들어 있는 엑셀로 받습니다.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Claude Skill](https://img.shields.io/badge/Claude-Skill-orange.svg)
[![DOI](https://zenodo.org/badge/1465056075.svg)](https://doi.org/10.5281/zenodo.24388715)

## 이 스킬로 할 수 있는 것

- **연구설계 판별 연습** — RCT, 군집 RCT, 비무작위 중재(비교군 있음·없음), 코호트, 분석적·기술적 횡단, 질적, 혼합까지 고를 수 있고, 어디에도 안 맞으면 "기타"에 직접 적습니다. Claude와 판별이 다르면 갈리는 지점을 짚는 질문으로 다시 생각해 봅니다.
- **뽑을 항목 스스로 정하기** — 어떤 항목을 추출하면 좋을지 먼저 적습니다. 공통 13개 항목과 설계별 추가 항목 중 빠뜨린 것은 Claude가 "왜 필요한지" 한 줄과 함께 제안합니다. 넣을 것과 뺄 것은 여러분이 고릅니다.
- **먼저 적고 비교하기** — 핵심 5개 항목(대상자·표본수·중재/변수/현상·종속변수와 측정도구·주요 결과)을 먼저 한 번에, 그다음 나머지를 네 개씩 묶어 값과 근거(페이지)를 적습니다. 그 뒤에 Claude의 값을 봅니다. 한 묶음이 정해져야 다음 묶음이 열립니다.
- **다른 값만 자세히 배우기** — 같은 뜻이면("94명"과 "총 94명") 한 줄로 넘어갑니다. 덜 적었으면 "적어 주신 것 / 제가 더 본 것 / 왜" 세 줄로 보완을 제안합니다. 숫자가 다르거나 변수·시점을 잘못 짚었으면 이 항목의 역할 → 논문의 근거 문장 → 왜 그 값인지 → 헷갈리기 쉬운 이유 순으로 설명을 읽고 최종값을 정합니다. 설명에 동의하면 "제안한 값으로 변경"만 누르면 되고, 원래 값을 유지하려면 이유를 적습니다.
- **엑셀로 받기** — 여러분의 값, Claude의 값, 최종값, 왜 달랐는지, 근거 위치가 모두 남습니다. 논문을 가로로 나란히 놓은 추출표와 항목 정의표도 들어 있습니다. 논문 1편이 끝날 때마다 자동으로 저장되고 다음 논문이 이어서 쌓입니다.
- **중간에 끊겨도 이어가기** — 저장된 엑셀과 PDF를 올리면 멈춘 항목부터 다시 시작합니다.

## 설치 및 사용 방법

1. literature-extraction-student.skill 다운로드
2. Claude.ai → 대화창 "+" 클릭 → 스킬 클릭 → 스킬 관리 클릭 → "추가" 클릭 → "스킬 업로드" 클릭 → 다운로드 받은 스킬 업로드
3. 새 대화에 논문 PDF 1편을 첨부하고 "+" 클릭 후 스킬 선택 후 Enter
4. 연구설계를 고르고 그렇게 판단한 문장과 페이지를 적습니다
5. 이 논문에서 뽑고 싶은 항목을 생각나는 대로 적고, Claude가 제안한 항목 중 넣을 것을 고릅니다
6. 묶음마다 나타나는 항목에서 "어디를 보세요"를 참고해 논문을 찾아 읽고, 값과 페이지를 적은 뒤 "계속"을 누릅니다
7. Claude의 값과 다른 항목은 설명을 읽고 최종값을 정합니다
8. 논문 1편이 끝나면 엑셀이 자동으로 옵니다 — 다음 논문을 첨부해 이어가고, 다 끝나면 "끝"이라고 입력합니다

대화가 끊겼으면 새 대화에 최신 엑셀과 PDF를 첨부하고 "이어서 해주세요."라고 하면 됩니다. 엑셀의 `_기록` 시트는 이어가기에 쓰이니 편집하거나 지우지 마세요.

## 사용하기 전에 알아 둘 것

- **먼저 적는 것이 핵심입니다.** Claude의 값을 보고 따라 적으면 배우는 게 없습니다. "어디를 보세요"를 따라 논문을 직접 찾아 읽고 적으세요. 틀려도 괜찮습니다 — 다른 값이 나온 항목에서 가장 많이 배웁니다.
- **"모르겠다"는 값이 아닙니다.** 못 찾겠으면 찾은 만큼만 적고 "못 찾겠음"이라고 쓰세요. Claude가 비교하면서 설명해 줍니다. 논문에 정말 없으면 NR(보고되지 않음)로 적습니다 — 추측으로 채우지 않습니다.
- **값마다 페이지를 적습니다.** 나중에 누가 봐도 어디서 가져왔는지 확인할 수 있어야 합니다. 초록에서만 본 값은 "(초록)"이라고 표시합니다.
- **Claude와 값이 같다고 정답은 아닙니다.** 일치율은 정확도의 지표가 아닙니다. 체계적 문헌고찰에서는 두 사람이 독립적으로 추출한 뒤 대조하며, 여기서는 Claude가 그중 한 사람 역할을 흉내 낼 뿐입니다. 과제·논문에는 생성형 AI의 도움을 받았다는 사실을 적으세요.

## 인용 및 출처

이 스킬 자체를 인용할 때는 아래 형식을 사용해 주세요(필요시):

Park S., Choe J., Woo K. (2026). literature-extraction-student: A Claude skill for learning data extraction in systematic reviews (Version 1.0) [Computer software]. ANDA Lab, Seoul National University College of Nursing. https://doi.org/10.5281/zenodo.24388715

## 라이선스

- 소스 코드 및 스킬 문서: [MIT License](https://github.com/rnrnrnn1234/literature-extraction-student/blob/main/LICENSE) © 2026 Soyeon Park
- 추출 항목 정의·설계 판별 기준·학습 안내 문구(`references/`): 제작자의 창작물로 MIT License에 포함됩니다

## 제작자

박소연 (Soyeon Park) — 서울대학교 간호대학 박사과정 · 스킬 설계·개발

rnsy1029@snu.ac.kr

최정인 (Jeongin Choe) — 수원과학대학교 조교수 · 검토·개선

choe2026@ssc.ac.kr

## 지도교수

우경미 (Kyungmi Woo) — 서울대학교 간호대학 부교수

ANDA Lab: https://andalab.snu.ac.kr/

## 감사의 말

이 도구는 AI 도구(Claude, Anthropic)를 활용하여 개발되었습니다. 모든 설계 결정, 요구사항 정의 및 검증은 제작자가 수행했습니다.

---

# Literature Data Extraction (Student) — Claude Skill (English)

A Claude skill for students practising data extraction for systematic reviews. Upload a paper and the questions appear one at a time in the chat, in order: what is the study design, what should be extracted, and what are the values. Each item comes with a note on where to look in the paper and what is easy to get wrong — use it to write your answer first. Then compare with the value Claude extracted independently. Where they differ, you get a full explanation: why this item is extracted, which sentence in the paper is the evidence, and why that value follows. If your answer is incomplete but not wrong, Claude only suggests what to add. The final decision is always yours. Results come back as an Excel file with the extraction table and your learning record.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Claude Skill](https://img.shields.io/badge/Claude-Skill-orange.svg)
![For Students](https://img.shields.io/badge/For-Students-5B8DEF.svg)
[![DOI](https://zenodo.org/badge/1465056075.svg)](https://doi.org/10.5281/zenodo.24388715)

## What you can do with this skill

- **Practise classifying study designs** — Choose from RCT, cluster RCT, non-randomized intervention (with or without a comparison group), cohort, analytical or descriptive cross-sectional, qualitative and mixed methods, or write your own under "other". If Claude's classification differs, a question pinpoints where the two readings part ways.
- **Choose the items yourself** — Write down which items you think should be extracted. Claude suggests anything you missed from the 13 common items and the design-specific add-ons, each with a one-line reason why it matters. You decide what goes in.
- **Write first, then compare** — You enter the five core items (participants, sample size, intervention/variables/phenomenon, dependent variables and instruments, main findings) first, then the rest in groups of up to four, each with a page number, before seeing Claude's values. The next group opens only after the current one is settled.
- **Learn from the ones that differ** — If the meaning is the same ("94" vs "n = 94 in total"), it moves on in one line. If yours is incomplete, Claude proposes an addition in three lines: what you wrote / what Claude also saw / why. If a number, group, variable or time point differs, you read a four-step explanation (what this item is for → the sentence in the paper → why that value → why it is easy to confuse) and make the final decision. If you agree, just choose "change to the suggested value"; to keep your own, give a reason.
- **Get it in Excel** — Your values, Claude's values, the final values, why they differed and where the evidence is are all kept, alongside a side-by-side extraction table and an item-definition sheet. It is saved automatically after each paper and the next paper is added to it.
- **Pick up where you left off** — Upload the saved Excel file and the PDF and you continue from the item where you stopped.

## Installation & Usage

1. Download literature-extraction-student.skill
2. In Claude.ai, click "+" in the chat box → Skills → Manage skills → Add → Upload skill → upload the downloaded file
3. In a new chat, attach one paper (PDF), click "+", select the skill and press Enter
4. Choose the study design and give the sentence and page that led you to it
5. List the items you want to extract, then pick from the items Claude suggests
6. For each group of items, use "where to look" to find and read the relevant part of the paper, enter the value and page number, and click Continue
7. Where Claude's value differs, read the explanation and decide the final value
8. After each paper the Excel file arrives automatically — attach the next paper to continue, and type "끝" (done) when you are finished

If the chat was interrupted, attach the latest Excel file and the PDF in a new chat and ask to continue. The `_기록` sheet in the Excel file is used for resuming, so do not edit or delete it.

## Before you start

- **Writing first is the point.** If you look at Claude's value and copy it, you learn nothing. Follow "where to look", read the paper yourself and write. It is fine to be wrong — you learn most from the items that differ.
- **"I don't know" is not a value.** Write what you did find and add "못 찾겠음" (could not find). Claude will explain while comparing. If the paper really does not report it, write NR (not reported) — never fill a gap by guessing.
- **Every value gets a page number.** Anyone should be able to check where it came from. Mark values seen only in the abstract as "(abstract)".
- **Agreeing with Claude does not mean you are right.** The agreement rate is not a measure of accuracy. In a systematic review two reviewers extract independently and reconcile; here Claude only stands in for one of them. State that you used generative AI assistance in assignments and manuscripts.

## Citation & Attribution

If you wish to cite this skill itself, please use the following format:

Park S., Choe J., Woo K. (2026). literature-extraction-student: A Claude skill for learning data extraction in systematic reviews (Version 1.0) [Computer software]. ANDA Lab, Seoul National University College of Nursing. https://doi.org/10.5281/zenodo.24388715

## License

- Source code and skill documentation: [MIT License](https://github.com/rnrnrnn1234/literature-extraction-student/blob/main/LICENSE) © 2026 Soyeon Park
- Item definitions, design-classification criteria and teaching text (`references/`): original work by the author, included under the MIT License

## Authors

Soyeon Park (박소연) — Doctoral Student, College of Nursing, Seoul National University · Design and development

rnsy1029@snu.ac.kr

Jeongin Choe (최정인) — Assistant Professor, Suwon Science College · Review and improvement

choe2026@ssc.ac.kr

## Advisor

Kyungmi Woo (우경미) — Associate Professor, College of Nursing, Seoul National University

ANDA Lab: https://andalab.snu.ac.kr/

## Acknowledgements

Developed with the assistance of AI tools (Claude, Anthropic). All design decisions, requirements, and validation were performed by the authors.
