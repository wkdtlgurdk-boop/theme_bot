# theme_bot

매일의 테마 카드 이미지가 쌓이는 곳. **코드는 여기 없다.**

카드를 만들고 스레드에 올리는 코드는
[`naver-sheets-autofill`](https://github.com/wkdtlgurdk-boop/naver-sheets-autofill)
의 `cards.py` / `post_threads.py` 에 있다. 그쪽 워크플로가 평일 16:00 KST 에
시트를 쓴 다음, 같은 데이터로 카드를 그려 이 리포에 밀어 넣는다.

```
cards/YYYYMMDD/01_monthly.png   하루 요약 (지수 + 테마 순위)
cards/YYYYMMDD/02_<테마>.png    테마별 카드, 거래대금 순
```

## 이 리포가 public 인 이유

스레드(Threads) API 는 이미지 업로드를 받지 않는다. 공개된 URL 을 주면 메타
서버가 그 URL 을 가져간다. 그래서 카드가 먼저 여기 올라가고,
`raw.githubusercontent.com/wkdtlgurdk-boop/theme_bot/main/cards/...` 주소로
게시된다. 비공개로 돌리면 게시가 깨진다.

## 2026-09-10 기록

원래 카드 봇은 사용자 PC 안에만 있었고, 그 PC 가 그래픽카드 고장으로 켜지지
않게 되면서 코드가 사라졌다. 이 리포에는 결과 PNG 만 올라와 있었고 드라이브
백업도 없었다 — 그래서 9/4·9/7·9/8 카드를 픽셀 단위로 재서 다시 만들었다.
`naver-sheets-autofill/test_cards.py` 가 그때 잰 좌표를 기준표로 들고 있다.

**이 리포의 PNG 를 지우지 말 것.** 게시된 스레드 글이 이 URL 을 가리키고
있고, 카드 디자인의 유일한 원본 기록이기도 하다.
