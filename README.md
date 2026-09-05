# search-tracker-report

검색량 추적 차트를 공개하기 위한 배포 전용 레포. **여기서 직접 작업하지 않는다.**

차트: https://lhwmath-integrate.github.io/search-tracker-report/

## 이 레포의 역할

수집 코드와 원본 데이터는 비공개 레포 `lhwmath-integrate/search-tracker`에 있다. GitHub Pages로 링크를 공유하려면 레포가 공개여야 하는데, 본체를 공개하면 추적 키워드와 수집 데이터까지 드러난다. 그래서 **차트 HTML 한 장만** 이쪽으로 밀어 보낸다.

## 동작

`search-tracker`의 `daily.yml`이 매일 KST 자정에 수집을 마친 뒤, 생성한 차트를 이 레포의 `gh-pages` 브랜치로 배포한다. 배포는 `force_orphan` 방식이라 브랜치 내용을 매번 통째로 교체한다.

그래서 이 레포에 파일을 직접 추가해도 다음 배포 때 사라진다. 이 README도 본체 레포의 `docs/report-repo-README.md`를 워크플로가 함께 배포하는 것이다. 고치려면 본체 레포에서 고쳐야 한다.

커밋이 항상 1개로 보이는 것도 같은 이유다.

## 차트 읽는 법

날짜는 **그 하루의 활동**이다. 수집은 자정 직후에 돌면서 직전 24시간을 세므로, 표시 날짜는 수집일 하루 전이다.

빈 날짜는 그날 수집이 실패했다는 뜻이다.
