# 파트5. 클래스와 객체

<br>

## 📚 목차

1. [문자열 검색 변환기 만들기](#-대제목1)
2. [대제목2](#-대제목2)
3. [대제목3](#-대제목3)
4. [대제목4](#-대제목4)

<br>
<br>
<br>
<br>

---

<br>
<br>
<br>
<br>
<br>

# 📌 문자열 검색 변환기 만들기

<br>

<br>
<br>
<br>

```java
문제: 문자열 검색 변환기 만들기

요구사항:
1. StringConverter 클래스를 만드세요.
2. 클래스는 문자열을 저장할 수 있는 String[] 또는 List<String>을 필드로 가집니다. (선택 가능)
3. 다음 기능들을 구현하세요:

기본 기능:
- 생성자는 쉼표(,)로 구분된 문자열을 받아서 배열 또는 리스트로 변환
- 문자열의 앞뒤 공백은 제거
- 빈 문자열은 저장하지 않음
- printAll() 메서드로 모든 문자열 출력

검색 기능:
- searchByKeyword(String keyword) : 특정 키워드를 포함하는 문자열들만 출력
- searchByPrefix(String prefix) : 특정 문자로 시작하는 문자열들만 출력

필요한 기능:
- printAll()
- searchByKeyword(String keyword)
- searchByPrefix(String prefix)


실행 예시:
StringConverter converter = new StringConverter("자바, 스프링,  파이썬, 자바스크립트, ");
converter.printAll();
// 출력:
// 자바
// 스프링
// 파이썬
// 자바스크립트

// 키워드 검색
converter.searchByKeyword("자바");
// 출력:
// 자바
// 자바스크립트

// 접두사 검색
converter.searchByPrefix("스");
// 출력:
// 스프링

출력 형식:
- 각 메서드는 찾은 결과가 없을 경우 "검색 결과가 없습니다." 출력
- 검색 결과는 한 줄에 하나의 문자열씩 출력
```

<br>
<br>

## 🎉 해결

<br>
<br>

# 📌 아이패드 대여 요금 계산기 만들기

<br>

<br>
<br>
<br>

```java
문제: 아이패드 대여 요금 계산기 만들기

요구사항:
1. TabletRentalCalculator 클래스를 구현하세요
2. 다음 기능들을 포함해야 합니다:


클래스 필드:
- 총 대여 가능한 아이패드 수량을 static 필드로 관리 (초기값: 20대)
- 현재까지의 총 대여 수익을 static 필드로 관리


대여 요금 규칙:
- 기본 요금: 1일 5000원
- 7일 이상 대여시: 1일당 4000원으로 할인
- 14일 이상 대여시: 1일당 3500원으로 할인
- 30일 이상 대여시: 1일당 3000원으로 할인


구현할 메서드:
1. calculateFee(int days)
  - 대여 일수를 받아서 총 요금을 계산
  - 예: 5일 대여 = 25000원 (5000원 × 5일)
  - 예: 10일 대여 = 40000원 (4000원 × 10일)


2. getDiscountRate(int days)
  - 대여 일수에 따른 일일 요금 반환
  - 예: 5일 → 5000원
  - 예: 10일 → 4000원


3. rentTablet(int days)
  - 아이패드 1대를 대여하고 재고를 감소시킴
  - 대여 불가능한 경우(재고 부족) 메시지 출력
  - 성공 시 대여 요금 반환하고 총 수익에 추가


4. static 메서드 추가:
  - getAvailableTablets(): 현재 대여 가능한 아이패드 수량 반환
  - getTotalRevenue(): 현재까지의 총 대여 수익 반환


실행 예시와 출력:

// 객체 생성
TabletRentalCalculator calc = new TabletRentalCalculator();

// 5일 대여
calc.rentTablet(5);

// 출력:
대여 일수에 따른 일일 요금: 5000원
계산된 총 대여 요금: 25000원 (5000원 × 5일)
대여가 완료되었습니다.
대여 기간: 5일
결제 금액: 25000원
남은 재고: 19대


// 10일 대여 (할인 적용)
calc.rentTablet(10);

// 출력:
대여 일수에 따른 일일 요금: 4000원 (7일 이상 할인 적용)
계산된 총 대여 요금: 40000원 (4000원 × 10일)
대여가 완료되었습니다.
대여 기간: 10일
결제 금액: 40000원
남은 재고: 18대


// 30일 대여 (추가 예시)
calc.rentTablet(30);

// 출력:
대여 일수에 따른 일일 요금: 3000원 (30일 이상 할인 적용)
계산된 총 대여 요금: 90000원 (3000원 × 30일)
대여가 완료되었습니다.
대여 기간: 30일
결제 금액: 90000원
남은 재고: 16대


// 재고 확인
// static 메서드를 호출해 주세요.
getAvailableTablets() 메서드 호출,
getTotalRevenue() 메서드 호출

// 출력:
현재 남은 재고: 18대
현재까지의 총 수익: 65000원




// 잘못된 일수 입력 (0일 이하)
calc.rentTablet(0);

// 출력:
대여 일수는 1일 이상이어야 합니다.

// 재고가 0일 때 대여 시도
[재고가 0일 때]
calc.rentTablet(1);

// 출력:
죄송합니다. 현재 대여 가능한 아이패드가 없습니다.
남은 재고: 0대
```

<br>
<br>

## 🎉 해결

<br>
<br>
