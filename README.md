# Get_pants_and_run
##### 2019 인터페이스 프로그래밍 전시회, 게임 개발 프로젝트 "빤쓰런"
* 유니티와 C#을 이용하여 달리기 2D 게임을 개발합니다!
* 회의록은 구글문서로 작성된 후 README에 업데이트합니다.
https://docs.google.com/document/d/1JyzNHxiSKBxWVrs8LKE3k4qC2CC7cksl2KVZuHQEcSg/edit#


## 1. 팀원

|이름|기수|학과|github ID|역할|
|:----:|:----:|:----:|:----:|:----:|
| 김태균 | 32기 | 전자정보통신공학과 | [WhiskyHolic](https://github.com/WhiskyHolic)| 개발|
| 김혜율 | 32기 | 소프트웨어학과 | [kcw1025](https://github.com/kcw1025)| 개발|
| 동기창 | 32기 | 전자정보통신공학과 | [ddongvanana](https://github.com/ddongvanana)| 디자인|
| 류국봉 | 31기 | 컴퓨터공학과 | [organicnameko](https://github.com/organicnameko)| 개발|
| 오재연 | 32기 | 전자정보통신공학과 | [jaeyonoj](https://github.com/jaeyonoj)| 개발|
| 이현주 | 31기 | 컴퓨터공학과 | [alro923](https://github.com/alro923)| 개발|
| 최우석 | 31기 | 전자정보통신공학과 | [wooseok1212](https://github.com/wooseok1212)| 디자인|

## 2. 개발 환경
* 개발 언어 : C#
* Unity : https://unity3d.com/kr/get-unity/download
* Visual Studio : https://docs.microsoft.com/ko-kr/visualstudio/install/install-visual-studio?view=vs-2019

## 3. 참고 강의
* Unity로 배우는 C# : https://programmers.co.kr/learn/courses/1
* How to make a 2d Platformer : https://www.youtube.com/watch?v=UbPiCgCkHTE

## 4. 기획
### 전체 구성
  - 메인 캐릭터 (빤쓰런 쳐야지~~)
  - 왼쪽에서 친구캐릭터가 쫓아옴 (너 나랑 밥먹기로 했잖아!!)
  - 생명 3개
  - 친구캐릭터가 던진 노트북/마우스를 맞거나, 학식을 밟거나, 오리랑 부딪히면 생명이 깎인다.
  - 피버타임에는 빤쓰를 벗어서 손에 들고 뛴다. 장애물이랑 부딪히면 다 부숴버린다!
  - 맵은 고정. 장애물도 고정. 맵 마지막에 보스가 등장!
  - 보스는 왼쪽에서 등장
  - 보스가 공격하며 쫓아오다가 일정 시간이 지쳐서 나가떨어짐.
   - 코인은 빤쓰를 구매하는 용도로 쓰인다. (보급팬티 -> 호피무늬 팬티 -> 날개달린 팬티)
  - 보스를 깨면 코인을 준다.  + 먹으면 코인준다
  - 템을 장착하면 보조 능력치가 생김
      - ex) 속도변화, 점프 횟수 추가
  - 점프랑 슬라이드 버튼 구현 (2단 점프가 기본)
  - 나중에 이스터에그로 구덩이를 통해 아래층으로 내려가게 할 것임

### Stage는 총 5단계, Stage마다 배경 달라짐
- 프롤로그
  - 학생회관 518호(동방)에서 밥먹기로 약속을 함
  - 친구들은 동방에 있고, 메인 캐릭터가 문틈으로 지켜보다가 도망침
  - 도망치는 메인캐를 친구들이 쫓아가면서 스토리가 진행됨
- Stage1
  - 컨셉 : 학생회관 5층 ~ 1층까지 맵이 구성됨. 계단 내려가는 애니메이션으로 화면 전환.
  - 배경 : 복도
  - 보스 : 세종냥이 :octocat:
- Stage2
  - 컨셉 : 센 B1층 ~ 1층까지 맵이 구성됨. 친구캐릭터가 노트북이나 마우스를 던져서 공격.
    - 친구가 야 저기있다!! 해서 엘베타고 꼭대기까지 올라가서 낙하산타고 연못으로 다이빙
  - 배경 : 컴퓨터실
  - 보스 : 거울 연못에서, AI가 보스(이면 좋을듯)
- Stage3
  - 컨셉 : 오리들이 사는 세종대 연못 주위를 돌아다님
  - 배경 : 보스전 아닐때는 연못 주위, 보스전에서는 연못 안으로 들어감 (메이플 아쿠아리움처럼 점프 무제한, 메인캐 모션은 
  - 보스 : 세종 오리
- Stage4
  - 컨셉 : 학식 혼밥하려는데 친구가 같이먹자고 쫓아옴
  - 배경 : 학생회관 지하1층 학생식당
  - 보스 : 친구가 학식 던져서 공격함. 맞거나 밟으면 생명 깎임
- Stage5
  - 컨셉 : 지하철을 타고 도망감, 어대역 6번 출구로 들어가서 건대입구역까지 가면 깨는 거임
    - '닉네임'은 빤쓰런에 성공했다!! 라는 문구가 뜨고 게임이 끝남 (Clear!)
  - 배경 : 지하철 1-1에 들어가서 8-4까지(맞나) 달리는 것임
  - 보스 : 열심히 쫓아오는 친구...

## 5. 스터디
> 매주 금요일 4시에 회의 및 스터디 (1~2시간)

> 19.09.01 ~ : 매주 월요일 && 화요일 오후 6시부터 회의 및 스터디 (2~3시간)

* 디자인
    * [ ] 프로토 타입 디자인
* 개발
    * [X] [Unity로 배우는 C#](https://programmers.co.kr/learn/courses/1) 강의 시청
    * [X] 키 입력받아서 GameObject 이동하는 과제
    * [X] 시작 위치로부터 이동한 거리 게임뷰에 숫자로 보여주기 (ex 달린거리 : XXXm)
    * [X] 상하 방향키 입력받아서 오브젝트(Ball)가 점프하도록 만들기 (3D 맵에 장애물도 만들어서 뛰어넘을수 있도록하기)
    * [ ] 오브젝트(Ball)가 맵에서 기본속도로 달리는 상황에서 특정 키를 누르면 10초동안 가속하게 만들기
    * [X] 맵에 코인 배치해놓고, 코인 먹으면 몇 개 먹었는지 게임뷰에 띄우기
    * [X] 캐릭터를 쫓아오는 몬스터 만들기
