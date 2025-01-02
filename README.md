# 응답하라 (Respond)

사용자들이 자신의 마이페이지를 자유롭게 꾸미고, 소통할 수 있는 플랫폼입니다.
개인적인 게시판, 방명록, 스케줄 관리 기능을 통해 일상적인 소통을 즐기고,
다양한 설정을 통해 자신의 공간을 개성 있게 꾸며보세요!

<br/>

# 🔥배포 링크

[Respond <응답하라>](https://respond-woad.vercel.app/)

| ID | test@test.com
-----|----------
| PW | testtest

<br/>
<br/>

# 📦폴더 구조

<details>
<summary>📦src</summary>

```
 ┣ app
 ┃ ┣ (auth)
 ┃ ┃ ┣ login
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┗ signup
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┣ [userId]
 ┃ ┃ ┣ board
 ┃ ┃ ┃ ┣ [postId]
 ┃ ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ chat
 ┃ ┃ ┃ ┣ [roomId]
 ┃ ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ playlist
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ schedule
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ setting
 ┃ ┃ ┃ ┣ components
 ┃ ┃ ┃ ┃ ┣ HomeSkelton.tsx
 ┃ ┃ ┃ ┃ ┣ SettingPrivacy.tsx
 ┃ ┃ ┃ ┃ ┣ SettingShowList.tsx
 ┃ ┃ ┃ ┃ ┗ SettingTabList.tsx
 ┃ ┃ ┃ ┣ hooks
 ┃ ┃ ┃ ┃ ┣ useGetUserIds.ts
 ┃ ┃ ┃ ┃ ┣ usePrivacyState.ts
 ┃ ┃ ┃ ┃ ┣ useSettingPrivacy.ts
 ┃ ┃ ┃ ┃ ┣ useSettingShowList.ts
 ┃ ┃ ┃ ┃ ┗ useSettingTabList.ts
 ┃ ┃ ┃ ┣ server-action
 ┃ ┃ ┃ ┃ ┣ playlistAction.ts
 ┃ ┃ ┃ ┃ ┗ settingAction.ts
 ┃ ┃ ┃ ┗ page.tsx
 ┃ ┃ ┣ layout.tsx
 ┃ ┃ ┗ page.tsx
 ┃ ┣ GlobalError.tsx
 ┃ ┣ favicon.ico
 ┃ ┣ globals.css
 ┃ ┣ layout.tsx
 ┃ ┗ page.tsx
 ┣ chatStyle
 ┃ ┗ styles.css
 ┣ components
 ┃ ┣ globalslayout
 ┃ ┃ ┣ GlobalsNav.tsx
 ┃ ┃ ┗ GlobalsUserInfo.tsx
 ┃ ┣ home
 ┃ ┃ ┣ BoardPrev.tsx
 ┃ ┃ ┣ ChatPrev.tsx
 ┃ ┃ ┣ Follow.tsx
 ┃ ┃ ┣ FollowComponent.tsx
 ┃ ┃ ┣ PlaylistPrev.tsx
 ┃ ┃ ┗ SchedulePrev.tsx
 ┃ ┣ playlist
 ┃ ┃ ┣ MyPlayList.tsx
 ┃ ┃ ┣ MyPlayListEdit.tsx
 ┃ ┃ ┣ PlayListModalBtn.tsx
 ┃ ┃ ┣ PlayTrackPreview.tsx
 ┃ ┃ ┣ Player.tsx
 ┃ ┃ ┣ PlaylistAll.tsx
 ┃ ┃ ┗ PlaylistSearch.tsx
 ┃ ┣ post
 ┃ ┃ ┣ createPost.tsx
 ┃ ┃ ┗ postList.tsx
 ┃ ┣ providers
 ┃ ┃ ┗ TQProvider.tsx
 ┃ ┣ searchBar
 ┃ ┃ ┣ RelatedSearchTerms.tsx
 ┃ ┃ ┗ UserSearchBar.tsx
 ┃ ┣ theme
 ┃ ┃ ┣ ThemeBtn.tsx
 ┃ ┃ ┗ ThemeModal.tsx
 ┃ ┣ ui
 ┃ ┃ ┣ LoadingSpinner.tsx
 ┃ ┃ ┣ checkbox.tsx
 ┃ ┃ ┣ label.tsx
 ┃ ┃ ┗ radio-group.tsx
 ┃ ┗ LogOutButton.tsx
 ┣ constants
 ┃ ┗ postSchema.ts
 ┣ hooks
 ┃ ┣ queries
 ┃ ┃ ┣ post
 ┃ ┃ ┃ ┗ usePostQuery.ts
 ┃ ┃ ┗ queryKeys.ts
 ┃ ┣ useFollow.ts
 ┃ ┣ useGetUserInfo.ts
 ┃ ┣ useLoggedIn.ts
 ┃ ┗ useOnAuthStateChange.ts
 ┣ lib
 ┃ ┗ utils.ts
 ┣ queries
 ┃ ┗ queryKey.ts
 ┣ server-action
 ┃ ┗ followAction.ts
 ┣ services
 ┃ ┣ auth
 ┃ ┃ ┗ serverAction.ts
 ┃ ┗ post
 ┃ ┃ ┣ postsPaginate.ts
 ┃ ┃ ┗ serverAction.ts
 ┣ store
 ┃ ┗ useUserInfoStore.ts
 ┣ styles
 ┃ ┗ styles.css
 ┣ types
 ┃ ┣ playlist
 ┃ ┃ ┣ Spotify.ts
 ┃ ┃ ┗ playlist.ts
 ┃ ┣ follow.ts
 ┃ ┣ post.ts
 ┃ ┣ setting.ts
 ┃ ┗ userInfo.ts
 ┣ utils
 ┃ ┗ supabase
 ┃ ┃ ┣ client.ts
 ┃ ┃ ┣ middleware.ts
 ┃ ┃ ┣ server.ts
 ┃ ┃ ┗ user.ts
 ┗ middleware.ts
```

</details>

<br/>
<br/>

# 개발 일정

| 기간                | 활동                                                   |     
| ------------------- | ------------------------------------------------------ | 
| 24.10.10            | 프로젝트 기획 및 주제 선정, 피그마로 프레임아웃 구성   |     
| 24.10.10            | 페이지 및 기능별 담당 구분, 프로젝트 세팅              |     
| 24.10.10 ~ 24.10.17 | 기능 개발                                              |     
| 24.10.16 ~ 24.10.17 | 스타일 적용 및 반응형 작업                                
| 24.10.17 ~ 24.10.17 | 트러블 슈팅 및 데이터 작업, 오류 수정, 최종 병합, 배포 |     
| 24.10.10 ~ 24.10.17 | 총 개발 기간                                           |     

<br/>
<br/>

# 💻 개발 환경

<br/>

## Frontend

- ![Next.js](https://camo.githubusercontent.com/d4ff95c6c85e810b4acfe5dbf01bf2b44680cf75945b21a7e5438c87b473f2c6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4e6578742d626c61636b3f7374796c653d666f722d7468652d6261646765266c6f676f3d6e6578742e6a73266c6f676f436f6c6f723d7768697465) **Next.js**
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white) **JavaScript**
- ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) **HTML5**
- ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) **CSS3**

- ![Tanstack Query](https://img.shields.io/badge/TanstackQuery-FF4154?style=for-the-badge&logo=reactquery&logoColor=white) **TanStack Query**
- ![Zustand](https://img.shields.io/badge/Zustand-181818?style=for-the-badge) **Zustand**
- ![Tailwind CSS](https://camo.githubusercontent.com/b2eac0f505dfd05c25acf8c285b5eb346916090126c8836c6cbf9aeb754eac32/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f7461696c77696e646373732d2532333338423241432e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d7461696c77696e642d637373266c6f676f436f6c6f723d7768697465) **Tailwind CSS**
- ![](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white) **Axios**
- **React Hook Form**
- **Zod**
- **Lucide**
- **Shadcn**
- **Moment Timezone**

<br/>

## Backend & API

- **Supabase**
- **Spotify API**

<br/>

## Development Tools

- **Yarn Berry**

<br/>

<br/>

# 🔧 주요기능

<details>
<summary><h2>1️⃣ 회원가입 페이지 / 로그인 페이지</h2></summary>

![로그인/회원가입](https://github.com/user-attachments/assets/fea3b2d7-0c37-4339-8574-695219716834)

- 아이디, 비밀번호, 닉네임을 입력하여 회원가입 할 수 있습니다.
- 아이디, 비밀번호를 입력하여 로그인 할 수 있습니다.
</details>
 
<br/>

<details>
<summary><h2>2️⃣ 나의 홈피 메인페이지</h2></summary>

![메인페이지](https://github.com/user-attachments/assets/3bf7e7d9-b071-4d28-9773-6b831fbe95ba)

- 홈피 메인페이지에 미리보기 탭으로 다양한 서비스를 접근할 수 있습니다.

![음악재생](https://github.com/user-attachments/assets/11528514-91f1-4ad1-8a05-aac0399b03a2)

- 메인페이지의 대문인 좌측 테이블에 플레이리스트에서 대표로 지정한 곡을 재생할 수 있습니다.

![테마변경](https://github.com/user-attachments/assets/dcaad8f4-b141-4e1f-af82-49792c4da2b5)

- 사용자의 홈피 색상을 변경할 수 있습니다.

![게시물](https://github.com/user-attachments/assets/71b28adc-bedd-4f54-8139-4de786efd155)

- 게시물을 업로드하고 조회하고 삭제할 수 있습니다.

![채팅](https://github.com/user-attachments/assets/c7a14567-4a48-462e-8ff2-960734b4a16e)

- 다른 사용자와 방을 만들고 실시간으로 채팅할 수 있습니다.
- 방은 생성되고 삭제할 수 있습니다.

![스케줄관리](https://github.com/user-attachments/assets/f433aa71-0af3-4c9b-bfd2-cad01ca81048)

- 스케줄을 진행중, 완료됨, 취소됨의 상태로 관리할 수 있습니다.

![플레이리스트](https://github.com/user-attachments/assets/561c5acb-b75a-4560-943f-edbabaa725a7)

- 플레이리스트에 곡을 추가할 수 있습니다.
- 추가된 곡은 삭제 또는 내 홈피 대문에 대표 곡으로 지정할 수 있습니다.

![내설정](https://github.com/user-attachments/assets/4f80e6d1-6110-4582-92cd-72a2c1405a49)

- 홈피 메인페이지에 미리보기 탭의 공개하고 싶은 목록을 수정할 수 있습니다.
- 공개범위를 설정할 수 있습니다. (이웃/서로이웃/모두/비공개)
- 공개하고 싶은 네비 탭 목록만 보여줄 수 있습니다.
</details>

<br/>

<details>
<summary><h2>3️⃣ 팔로잉/팔로워 사용자 검색 기능</h2></summary>


![검색기능:팔로워기능](https://github.com/user-attachments/assets/338c7c28-1bde-4dd6-b61f-055b72e0ce8c)

- 사용자를 검색하고 사용자의 홈피에 진입할 수 있습니다.
- 팔로잉을 걸고 사용자가 공개한 게시물과 플레이리스트를 접근할 수 있습니다.
</details>

<br/>
<br/>

# 🏹 트러블 슈팅

<details>
<summary> <h2>1️⃣ 마이페이지 데이터 필터링</h2> </summary>

## 문제\_
api 노래목록별로 추가버튼 생성 후 클릭시 supabase에 데이터가 올라가야하는데 에러

## 원인\_
테이블의 각 행별로 설정상 null은 허용하지않는다 해두었다.
playlist에 값을 insert 해주면서 user_id 의 값을 넘겨주지않아, user_id 값이 null로 넘어가면서 생긴 문제

## 해결\_
browserClient.auth.getUser() : 로그인한 유저의 정보를 가져온다. -> 로그인한 유저가 없으면 유효성처리
playlist에 값을 insert하면서 user_id도 같이 넘겨준다.
=> 이 과정을 기존 패치로 구현한부분에서 텐스텍쿼리로 전체 변경한다

</details>
<br />

<details>
<summary><h2>2️⃣ docs 꼼꼼하게 읽지 않은 문제</h2></summary>

<img width="1000" alt="이원빈" src="https://github.com/user-attachments/assets/bd6580ff-cf25-4be9-8840-75af286d885f">

## 문제\_
server action에서 위처럼 클라이언트를 전역적으로 한번 선언하고 재사용하려고 하니 import { cookies } from "next/headers" 에서 에러가 발생했다.

<img width="1000" alt="이원빈2" src="https://github.com/user-attachments/assets/07323f05-6577-413e-9047-5ce048b12058">

## 해결\_

supabase를 자세히 보니 사용 시 마다 클라이언트를 만들라고 나와있었다.
</details>

<br />

<details>
<summary><h2>3️⃣ 저장된 유저 아이디(id)와 일치하는 nickname 가져와 보여주기</h2></summary>

## 문제\_
user_info의 id를 외래키로 설정해 participantIds 배열을 만들고 닉네임을 매칭시키지 않은 문제

![김서연](https://github.com/user-attachments/assets/c2ea837c-5bb2-4c81-98ec-145c4e2949f3)

## 해결\_
rooms 테이블에 저장된 참가자 아이디(participants) 와 user_info 테이블에 저장된 유저 아이디(id)와 일치하는 nickname 가져오기

![김서연-2](https://github.com/user-attachments/assets/9c140038-40a3-49d1-a34d-876ea02d13da)

## 결론\_
id와 일치하는 participant
(4d0d034b-c092-4b9e-bbdb-0d5b25e21cba) 찾아서 nickname 반환 성공!

### ↓ 더 자세한 ⚒️ 트러블슈팅 !

[![Velog's GitHub stats](https://velog-readme-stats.vercel.app/api?name=gimmari&tag=&color=dark)]([https://velog.io/@gimmari/트러블슈팅](https://velog.io/@gimmari/데이터를-한-형식에서-다른-형식으로-변환하는-데이터-매핑-Data-Mapping))

</details>

<br/>

<details>
<summary><h2>4️⃣ 유저 정보 가져오는 커스텀 훅 (TQ사용)</h2></summary>

![이준열](https://github.com/user-attachments/assets/87f45bbd-d4c2-4044-a32f-2926a3e9e206)

## 문제\_
특정 상황에서 유저 데이터가 다르게 들어옴. 어쩔땐 ID만, 어쩔땐 객체로

## 해결\_
유저 정보를 가져오는 TQ가 두 개 있었는데 같은 queryKey[“loginUser”] 를 공유했음. 따라서 다른 함수에서 다른 데이터를 요청하지만 같은 캐싱을 사용하기 때문에 발생했고, que 경하고 문제 해결
</details>
<br/>

<details>
<summary> <h2>5️⃣ user 상태가 초기에는 null인 이슈</h2></summary>

<img width="1000" alt="장수인" src="https://github.com/user-attachments/assets/b6253ca2-70ec-4081-a736-f2086c98f303">

## 문제\_
user 상태가 초기에는 null인 상태에서 fetchTodos 함수가 호출되기 때문에 사용자가 로그인하지 않았거나 API호출이 지연되면 todo 목록이 로드되지 않음

## 해결\_
fetchTodos 함수가 user 상태가 변경된 후에만 호출되도록 useEffect 의 의존성 배열에 user를 추가
</details>

