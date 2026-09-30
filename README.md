<!DOCTYPE html>
<html lang="mn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Нэг юм ярья 🍻</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;

            font-family: Arial, sans-serif;

            background: linear-gradient(135deg, #111, #4b1d00);
            overflow: hidden;
        }

        .card {
            width: 90%;
            max-width: 500px;

            background: rgba(255,255,255,0.95);
            padding: 40px 25px;

            border-radius: 25px;
            text-align: center;

            box-shadow: 0 20px 60px rgba(0,0,0,0.5);

            position: relative;
            z-index: 10;
        }

        .emoji {
            font-size: 70px;
        }

        h1 {
            color: #d35400;
            font-size: 30px;
        }

        p {
            color: #444;
            font-size: 18px;
            line-height: 1.6;
        }

        .message {
            background: #fff3e6;
            padding: 20px;
            border-radius: 15px;
            margin: 20px 0;
        }

        button {
            border: none;
            padding: 15px 25px;
            margin: 10px;
            border-radius: 30px;

            font-size: 17px;
            cursor: pointer;

            transition: 0.3s;
        }

        #drink {
            background: #d35400;
            color: white;
        }

        #drink:hover {
            transform: scale(1.1);
            background: #e67e22;
        }

        #no {
            background: #ddd;
            color: #444;
        }

        #result {
            display: none;
            margin-top: 25px;
            color: #d35400;
            font-size: 21px;
            font-weight: bold;
        }

        .beer {
            position: fixed;
            font-size: 35px;
            animation: fall 6s linear infinite;
            top: -50px;
        }

        @keyframes fall {
            0% {
                transform: translateY(0) rotate(0deg);
            }

            100% {
                transform: translateY(110vh) rotate(360deg);
            }
        }
    </style>
</head>

<body>

    <!-- Унаж байгаа emoji -->
    <div class="beer" style="left:10%; animation-delay:0s;">🍻</div>
    <div class="beer" style="left:30%; animation-delay:2s;">🥃</div>
    <div class="beer" style="left:55%; animation-delay:1s;">🍺</div>
    <div class="beer" style="left:80%; animation-delay:3s;">🍻</div>

    <div class="card">

        <div class="emoji">
            🍻😂
        </div>

        <h1>
            BRO, НЭГ ЮМ ЯРЬЯ...
        </h1>

        <p>
            Өнөөдөр орой завтай юу? 👀
        </p>

        <div class="message">

            Зүгээр ээ...

            <br><br>

            ГАНЦХАН хундага л ууя. 😂

            <br><br>

            Ганц гэдэг нь...

            <br>

            <b>магадгүй хэд хэдэн ганц. 🍻</b>

        </div>

        <p>
            За яах уу? 😏
        </p>

        <button id="drink" onclick="yes()">
            🍻 УУЯ
        </button>

        <button id="no" onclick="no()">
            😇 Үгүй ээ
        </button>

        <div id="result"></div>

    </div>

    <script>

        function yes() {

            document.getElementById("result").style.display = "block";

            document.getElementById("result").innerHTML =
                "HAHAHA 😂🍻<br><br>" +
                "ЧАМАЙГ Л ХҮЛЭЭЖ БАЙЛАА BRO 😂<br><br>" +
                "Гэхдээ хариуцлагатай ууна шүү 😎";

        }

        function no() {

            document.getElementById("result").style.display = "block";

            document.getElementById("result").innerHTML =
                "😐<br><br>" +
                "За за...<br>" +
                "Чи өнөөдөр их зөв хүн болох нь дээ 😂";

        }

    </script>

</body>
</html>
