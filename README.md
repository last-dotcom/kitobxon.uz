# kitobxon.uz
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WorldBook</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f2f4f8;
            color: #333;
            margin: 0;
            padding: 20px;
            transition: background-color 0.3s;
        }

        header {
            background-color: #007BFF;
            color: white;
            padding: 20px;
            text-align: center;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        h1 {
            margin: 0;
            font-size: 2.5em;
        }

        h2 {
            margin-top: 20px;
            color: #007BFF;
            font-size: 1.5em;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin: 10px 0;
        }

        a {
            text-decoration: none;
            color: #007BFF;
            transition: color 0.3s, transform 0.3s;
            padding: 10px;
            border-radius: 5px;
            display: inline-block;
            background-color: #fff;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            width: 100%; /* Mobil uchun kenglik */
            box-sizing: border-box; /* To'liq kenglikni hisoblash */
        }

        a:hover {
            color: #0056b3;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        footer {
            text-align: center;
            margin-top: 20px;
            font-size: 14px;
            color: #777;
        }

        /* From Uiverse.io by andrew-demchenk0 */ 
        button {
            position: relative;
            width: 130px;
            height: 35px;
            border-radius: 30px;
            background-color: white;
            border: 1px #08c solid;
            overflow: hidden;
            margin: 0 5px; /* Tugmalar orasidagi masofa */
        }

        .text1 {
            font-size: 15px;
            font-weight: 600;
            margin-left: 22%;
        }

        .text2 {
            position: absolute;
            top: 25%;
            left: -50px;
            font-weight: 700;
            font-size: 14px;
            color: white;
        }

        .icon {
            position: absolute;
            top: 0;
            left: 0;
            transition: transform 0.5s;
        }

        .icon::before {
            position: absolute;
            left: -100px;
            top: 0;
            z-index: -1;
            content: '';
            width: 130px;
            height: 33px;
            border-radius: 30px;
            background-color: #08c;
        }

        button:hover .icon {
            transform: translateX(96px);
            transition: transform 0.5s;
        }

        button:hover .text2 {
            transform: translateX(100px);
            transition: transform 0.6s;
        }

        button:active {
            transform: scale(1.03);
        }
    </style>
    <script>
        function showBooks(genre) {
            var allBooks = document.querySelectorAll('.book-genre');
            allBooks.forEach(function(book) {
                book.style.display = 'none'; // Barcha kitob bo'limlarini yashirish
            });
            var selectedBooks = document.getElementById(genre);
            if (selectedBooks) {
                selectedBooks.style.display = 'block'; // Tanlangan janr kitoblarini ko'rsatish
            }
        }

        function changeBackgroundColor() {
            // Tasodifiy rangni olish
            var randomColor = '#' + Math.floor(Math.random()*16777215).toString(16);
            document.body.style.backgroundColor = randomColor; // Orqa fon rangini o'zgartirish
        }
    </script>
</head>
<body>
    <header>
        <h1>Kitoblar Ro'yxati</h1>
        <p>O'zigzga kerak bolgan kitoblarni izlab topshigz mukun</p>
    </header>

    <main>
        <section class="book-list" id="book-list-section">
            <h2>Kitob Janrlari</h2>
            <ul>
                <li><a href="javascript:void(0);" onclick="showBooks('Badiy adabiyot')">Badiy adabiyot</a></li>
                <li><a href="javascript:void(0);" onclick="showBooks('dev')">Dasturchilar uchun</a></li>
                <li><a href="javascript:void(0);" onclick="showBooks('Tarix')">Tarix</a></li>
                <li><a href="javascript:void(0);" onclick="showBooks('Bolalar uchun')">Bolalar uchun</a></li>
                <li><a href="javascript:void(0);" onclick="showBooks('Sherlar')">Sherlar</a></li>
            </ul>
        </section>

        <section id="Bolalar uchun" class="book-genre" style="display: none;">
            <h2>Bolalar uchun</h2>
            <ul>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/Рус_халқ_эртаклари.pdf" target="_blank">Rus xalq ertaklari</a></li>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/bolalradabiyoti.pdf" target="_blank">Bolalar adabiyoti</a></li>
            </ul>
        </section>

        <section id="Sherlar" class="book-genre" style="display: none;">
            <h2>Bu bolimda kitoblaar yoq</h2>
            <ul>
                
            </ul>
        </section>

        <section id="Badiy adabiyot" class="book-genre" style="display: none;">
            <h2>Badiiy adabiyot</h2>
            <ul>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/Abdulhamid-Cholpon.pdf" target="_blank">Cholpon</a></li>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/AlisherNavoyi.pdf.pdf" target="_blank">Alisher Navoyi</a></li>
            </ul>
        </section>

        <section id="dev" class="book-genre" style="display: none;">
            <h2>dasturlash</h2>
            <ul>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/PGDCA-202_slm.pdf" target="_blank">Web application development PHP</a></li>
                <li><a href="file:///C:/Users/user/Downloads/Telegram%20Desktop/VS%20Code%20Shortcuts.pdf" target="_blank">VS code shortcuts CheatSHeet</a></li>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/Head%20First%20HTML%20and%20CSS%20(%20PDFDrive%20).pdf" target="_blank">Head First HTML and CSS ( PDFDrive )</a></li>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/Head%20First%20HTML%20and%20CSS%20(%20PDFDrive%20).pdf" target="_blank">Head First Javascript programming</a></li>
                <li><a href="file:///D:/1_web/01/otash.ai/kitob/web%20book/HTML%20and%20CSS%20design%20and%20build%20websites%20(John%20Duckett).pdf" target="_blank">HTML and CSS design and build websites (John Duckett)</a></li>
            </ul>
        </section> 

        <section id="Tarix" class="book-genre" style="display: none;">
            <h2>Xali bu bolimda Kitoblar yoq</h2>
            <ul>
             
            
            </ul>
        </section>
    </main>

    <footer>
        <button onclick="changeBackgroundColor()">Orqa fon rangini o'zgartirish</button>
        <a href="https://t.me/KitobSky_bot">
            <button> 
              <span class="icon"><svg xmlns="http://www.w3.org/2000/svg" width="33" viewBox="0 0 120 120" height="33" fill="none"><path fill="#08c" d="m60 0c-33.1373 0-60 26.8627-60 60s26.8627 60 60 60 60-26.8627 60-60-26.8627-60-60-60z"></path><path fill="#fff" d="m89.195 34.5144-10.7166 54.0314s-1.4985 3.7472-5.6203 1.9486l-24.7303-18.96-8.9925-4.3462-15.1378-5.0963s-2.3231-.824-2.5481-2.6226c-.2246-1.7986 2.6231-2.7727 2.6231-2.7727l60.1763-23.6062s4.9462-2.1731 4.9462 1.424z"></path><path fill="#d2e5f1" d="m46.2272 87.9392s-.7219-.0675-1.6215-2.9157c-.899-2.8476-5.4704-17.8353-5.4704-17.8353l36.3456-23.0814s2.0986-1.274 2.0236 0c0 0 .3745.2246-.7495 1.2736-1.1241 1.0495-28.5521 25.7044-28.5521 25.7044"></path><path fill="#b5cfe4" d="m57.6099 78.8041-9.7818 8.9184s-.7642.5804-1.6009.2167l1.8727-16.5662"></path></svg></span>
              <span class="text1">Telegram bot</span>
              <span class="text2">Kirish</span> 
            </button> </a>
        </a>
    </footer>
</body>
</html>
