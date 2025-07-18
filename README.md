<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>랜덤 점심 메뉴 추천</title>
    <style>
        /* 전체 배경과 폰트 설정 */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa, #c3cfe2);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
            justify-content: center;
            color: #333;
        }

        /* 컨테이너 박스 */
        .container {
            background-color: white;
            padding: 2rem 3rem;
            border-radius: 12px;
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
            text-align: center;
            max-width: 400px;
            width: 90%;
        }

        h1 {
            margin-bottom: 1rem;
            color: #4a90e2;
        }

        /* 메뉴 출력 영역 */
        #menuDisplay {
            font-size: 1.5rem;
            font-weight: bold;
            margin: 1.5rem 0;
            color: #e94e77;
            min-height: 2em;
        }

        /* 버튼 스타일 */
        button {
            background-color: #4a90e2;
            border: none;
            color: white;
            padding: 0.75rem 1.5rem;
            font-size: 1rem;
            border-radius: 8px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #357ABD;
        }

        /* 푸터 */
        footer {
            margin-top: 2rem;
            font-size: 0.9rem;
            color: #777;
        }
    </style>
</head>

<body>
    <div class="container">
        <h1>오늘의 점심 메뉴 추천</h1>
        <div id="menuDisplay">아래 버튼을 눌러 메뉴를 추천받으세요!</div>
        <button id="recommendBtn">메뉴 추천받기</button>
    </div>

    <footer>
        &copy; 2025 [작성자 이름]
    </footer>

    <script>
        // 1. 메뉴 이름들이 들어 있는 배열을 만드세요.
        //    예) ["김치찌개", "비빔밥", ...]
        const menus = [
            "김치찌개",
            "된장찌개","김치찌개",
            "된장찌개","김치찌개",
            "된장찌개","김치찌개",
            "된장찌개","김치찌개",
            "된장찌개","김치찌개",
            "된장찌개","김치찌개",
            "된장찌개"
        ];

        // 메뉴를 보여줄 위치를 가져옵니다. (아직 안 배움)
        const menuDisplay = document.getElementById('menuDisplay');
        const recommendBtn = document.getElementById('recommendBtn');

        // 버튼 클릭 시 다음 코드를 실행합니다. (아직 안 배움)
        recommendBtn.addEventListener('click', () => {
            // 2. 버튼 클릭 시 랜덤으로 메뉴를 선택하여 화면에 출력하세요.
            //    Math.random()을 사용하여 0부터 menus.length - 1까지의 정수를 생성하세요.
            const randomIndex = Math.floor(Math.random() * menus.length);
            // 3. menus 배열에서 랜덤으로 선택된 인덱스를 사용하여 메뉴를 가져옵니다.
            const selectedMenu = menus[randomIndex];
            // 4. 선택된 메뉴를 화면에 출력하세요.
            menuDisplay.textContent = `🍽 오늘의 메뉴는 ${selectedMenu} 입니다!`;
        });
    </script>
</body>

</html>
