# AutoCAD2023

## 오토캐드
- 확장자 : Dwt(기계번역), Dwg(인간번역), Bak(백업)
- 캐드 환경설정 초기화 : 윈도우 > 기본값으로 재설정 > 사용자설정 재설
  
## 도면의 크기와 척도
|A0|A1|A2|A3|A4|
|------|---|---|---|---|
|841 * 1189|594 * 841|420 * 594|297 * 420|210 * 297|
- 제도 용지 세로와 가로 비 : 1:1.414, A4의 크기로 절는 것을 원칙, A3 여백 최소 크기(철하지 않을 때 10mm, 철할 때 20mm)
- 표제란 내용 : 도면번호, 공사 명칭, 축척, 설계 책임자의 서명, 성명, 도면 작성날짜, 도면 분류 번호등), 윤관선 최소 0.5mm 이상 두께의 실선
- 척도 : 현척(1:1) 실물크기와 같게, 배척(50:1) 실물 크기보다 크게, 축척(1:2) 실물 크기보다 작게게

## 모양에 따른 종류 - 실선(외형선) > 파선(숨은선) > 중심선
|선 종류|비고|
|------|---|
|실선(Continue)|단면선, 외형선, 치수선, 치수 보조선, 지시선, 해칭선|
|파선(Hidden)|숨은선|
|1점 쇄선(Center)|중심선, 절단선, 경계선, 기준선|
|2점 쇄선(Phantom)|가상선|

## 굵기에 따른 종류
|선 종류|비고|
|------|---|
|가는선|기호선, 패턴선, 보조선 등|
|중간선|입면선, 가구선, 창호선 등|
|굵은선|벽체, 기둥 등의 단면선 등|

## 용도에 따른 종류
|선 종류|선 모양|비고|
|------|---|---|
|외형선(Visible)|굵은실선|물체의 보이는 부분을 나타내는 선|
|치수선(Dimension)|가는실선|치수를 기입하기 위한 선|
|치수 보조선 / 지시선<br/>(Extension) / (Leader)|가는실선|치수, 기호 등을 나타내기 위하여 끌어낸 선|
|해칭선 (Section)|가는실선|바닥의 패턴이나 마감재의 구분 및 물체의 절단면을 나타내는 선|
|파단선 (Break)|가는실선|부분 생략, 부분 단면의 경계를 나타내는 선|
|숨은선 (Hidden)|파선|물체의 보이지 않는 부분을 나타내는 선|
|중심선 (Center)|가는 1점 쇄선|도면이나 물체의 중심을 나타내는 선|
|가상선 (Phantom)|가는 2점 쇄선|움직이는 물체의 이동 후의 위치를 가상하여 나타내는 선|

- 디자인 요소 : 크기, 위치, 색상, 재질, 이동, 모양
  
## Lisp - 사용자 정의명령어
- Appload 등록
- mm 평,면적,길이
- Q 히든 처리
- QQ 히든 처리리

## F1 ~ F12
|키|기능|설명|
|------|---|---|
|F1|도움말|활성 툴팁, 명령, 팔레트 또는 대화상자에 대한 도움말을 표시|
|^F2|확장된 사용내역|명령 윈도우에 확장된 명령 사용 내역 표시|
|#F3|객체 스탭|객체 스냅을 켜거나 끈다|
|F4|3D 객체 스냅|3D용 추가 객체 스냅을 켜거나 끈다|
|F5|등각평면|2D 등각평면 설정을 순환|
|F6|동적 UCS|평면형 표면에 대한 자동 UCS 정렬을 켜거나 끈다|
|&F7|그리드 표시|그리드 표시를 켜거나 끈다|
|#F8|직교|커서 이동이 수평 또는 수직으로만 움직임|
|&F9|그리드 스냅|커서의 움직임을 지정된 그리드 간격으로 제한|
|F10|극좌표 추적|지정된 각도로 커서가 이동|
|^F11|객체 스냅 추적|객체 스냅 위치에서 수평 및 수직으로 커서를 추적|
|F12|동적 입력|커서 주위에 거리와 각도를 표시하고 탭을 사용하여 필드 간을 이동하면 입력한 내용이 적용|


## 자주사용하는 명령어 모음
|명령어|용도|명령어|용도|명령어|용도|명령어|용도|
|------|---|---|---|---|---|---|---|
|Line|선 그리기|EXtend|물체의 연장|MText|다중행 문자 입력|Ctrl + S|도면의 저장|
|Circle|원 그리기|MIrror|물체의 대칭 복사|DText|단일행 문자 입력|Ctrl + N|새로운 도면의 작성|
|Arc|원호 그리기|Move|물체의 이동|DIst|길이•각도 측정|Ctrl + O|도면 열기|
|RECTANG|사각형 그리기|COpy|물체의 복사|BHatch|해칭하기(대화상자)|Ctrl + Shift + C|기준점 복사|
|POLygon|다각형 그리기|BReak|물체의 절단|DDEDIT|문자편집|Ctrl + Shift + V|기준점 붙혀넣기|
|REgen|사라진 도면 재생성|ROtate|물체의 회전|TestSTyle|문자 스타일 정하기|Startup 0|시작화면구성|
|Zoom|화면 확대 및 축소(전체A,범위E,객체O)|ARray|물체의 배열 복사|LAyer|레이어 설정|Rlbbon-close|화면 탭 구성|
|Pan|화면 이동, 고정|Stretch|물체의 줄이고 늘이기|LineType|라인 타입 설정|UNit|도면단위|
|SCale|물체의 크기 조절|CHAmfer|모서리의 모따기|PLine|폴리라인 그리기|||
|Erase|도면요소의 삭제|Fillet|모서리의 라운딩|PEdit|폴리라인 편집|OP|옵션창|
|Undo|이전 실행명령 취소|eXplode|도면 요소의 분해|PIOT|출력하기|||
|OSnap|물체의 특정점 찍기|MLine|다중선 그리기|||||
|Offset|물체의 수평 복사|DOnut|도넛 그리기|||||
|TRim|교차부 끊어내기|EIlipse|타원 그리기|||||
|||||||||
|||||||||
|||||||||
