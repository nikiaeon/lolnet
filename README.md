
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой сайт</title>
    <link rel="stylesheet" href="1.css">
    <script src="1.js"></script>
</head>
<body>
<nav>
  <ul>
    <li><a href="index.html">Главная</a></li>
    <li><a href="news.html">Новости</a></li>
    <li><a href="contacts.html">Контакты</a></li>
    <li><a href="prof.html">Профиль</a></li>
  </ul>
</nav>
<div class="area">
    <h1 align="center"><font color="green" face="Mv boli" size="15px">L</font> <font color="#B0E0E6" face="Mv boli" size="5px">oLNet</font></h1>
    <ul class="circles">
        <li>❤️️Оля❤️️</li>
        <li>Я люблю Олю🌸</li>
        <li>Оля моя любовь🌹</li>
        <li>Дорогая Оля🌺</li>
        <li>Оля❤️️</li>
        <li>Оля💘</li>
        <li>Оля</li>
        <li>Радость Оля</li>
        <li>❤️️</li>
        <li>❤️️</li>
    </ul>
</div>

<script>
    // Получаем имя пользователя из локального хранилища
    var username = localStorage.getItem('username');

    // Проверяем, сохранено ли имя пользователя в локальном хранилище
    var isLoggedIn = username !== null;

    // Проверяем, не находимся ли мы уже на странице регистрации
    var isOnRegistrationPage = window.location.href.includes('index.html');

    // Если пользователь не авторизован и не находится на странице регистрации, перенаправляем его на страницу регистрации
    if (!isLoggedIn && !isOnRegistrationPage) {
        console.log("Пользователь не авторизован, перенаправляем на страницу регистрации.");
        window.location.href = 'reg.html'; // Поменяйте на правильное имя файла
    } else 
    {
        // Если пользователь авторизован, выводим приветственное сообщение
        var welcomeMessage = username !== null ? "Привет, " + username + "!" : "Добро пожаловать!";
        alert(welcomeMessage);
    }
</script>


    <style>
    
/* Стили для второго меню */
.second-menu {
    position: absolute;
    background-color: rgba(240, 240, 240, 0.5); /* Увеличим прозрачность фона */
    border: 3px solid #008000; /* Зеленая обводка */
    border-radius: 15px; /* Скругляем углы */
    padding: 20px; /* Отступы внутри окна */
    display: none;
    z-index: 9998;
    font-family: Arial, sans-serif; /* Заменим на Arial для более стандартного шрифта */
    top: 120px; /* Немного увеличим отступ сверху */
    left: 12%; /* Центрируем по горизонтали */
    transform: translateX(-50%); /* Смещаем на половину ширины элемента влево */
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1); /* Уменьшим тень */
}

/* Стили для кнопок второго меню */
.second-menu button {
    display: block;
    margin-bottom: 10px;
    padding: 12px 24px; /* Увеличим отступы внутри кнопок */
    cursor: pointer;
    font-family: Arial, sans-serif; /* Заменим на Arial для более стандартного шрифта */
    border-radius: 8px; /* Закругляем углы */
    box-shadow: 0 2px 3px rgba(0, 0, 0, 0.1); /* Уменьшим тень */
    background-color: rgba(240, 240, 240, 0.5);
    border: 2px solid #008000; /* Зеленая обводка */
    color: #008000; /* Зеленый цвет текста */
    transition: all 0.3s ease; /* Плавное изменение стилей */
}

/* Стили для кнопок второго меню при наведении */
.second-menu button:hover {
    background-color: #008000; /* Зеленый фон при наведении */
    color: #ffffff; /* Белый цвет текста при наведении */
}

        /* Стили для содержимого центрированного окна */
        .centered-window {
            position: fixed;
            top: 50%;
            left: 50%;
            right: 50px;
            transform: translate(-50%, -50%);
            background-color: rgba(240, 240, 240, 0.5); /* Частично прозрачный серый цвет фона */
            border: 2px solid #008000; /* Зеленая обводка */
            box-sizing: border-box;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
            font-family: sans-serif;
            z-index: 9999;
            display: none; /* Изначально скрываем окно */
        }

        /* Стили для кнопки открытия второго меню */
        .info-button {
            position: absolute;
            left: 20px; /* Располагаем по левому краю */
            top: 15px; /* Отступаем сверху */
            background-color: #ffffff;
            border: 2px solid #000000;
            padding: 10px 20px;
            cursor: pointer;
            z-index: 9999;
            font-family: sans-serif;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        
        /* Стили для полосы прокрутки */
.centered-window {
    /* Добавляем полосу прокрутки только при необходимости */
    overflow: auto;
}

/* Стили для WebKit (Chrome, Safari, Opera) */
.centered-window::-webkit-scrollbar {
    width: 12px;
}

.centered-window::-webkit-scrollbar-track {
    background: #f1f1f1;
}

.centered-window::-webkit-scrollbar-thumb {
    background: #555;
    border-radius: 6px;
}

.centered-window::-webkit-scrollbar-thumb:hover {
    background: #333;
}

/* Стили для Firefox */
.centered-window {
    scrollbar-width: thin;
    scrollbar-color: #555 #f1f1f1;
}

.centered-window::-webkit-scrollbar-track {
    background: #f1f1f1;
}

.centered-window::-webkit-scrollbar-thumb {
    background-color: #555;
    border-radius: 6px;
    border: 3px solid #f1f1f1;
}

.centered-window::-webkit-scrollbar-thumb:hover {
    background-color: #333;
} 
    </style>




<style>
/* цвет кнопки НАЗАД при наведении курсора */
.back-button {
    background-color: #4CAF50; /* Зеленый цвет кнопки */
    border: none;
    color: white;
    padding: 5px 20px; /* Поля вокруг текста */
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 10px 2px;
    height: 40px;
    cursor: pointer;
    border-radius: 5px; /* Закругление углов */
    transition: background-color 0.5s ease;
}

.back-button:hover {
    background-color: #800000; /* цвет кнопки при наведении курсора */
}

</style>


<style>
/* Стили для кнопок */
.styled-button {
    background-color: #4CAF50; /* Зеленый цвет */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
}

/* Стили для различных типов кнопок */
.button1 {
    background-color: #4CAF50; /* Зеленый цвет */
}

.button2 {
    background-color: #008CBA; /* Синий цвет */
}

.button3 {
    background-color: #f44336; /* Красный цвет */
}
</style>




<style>
/* Стили для полосы прокрутки */
/* Для браузеров на основе WebKit (например, Chrome, Safari) */
/* Общие стили для всех состояний полосы прокрутки */
::-webkit-scrollbar {
    width: 10px; /* Ширина полосы прокрутки */
}

/* Стили для полосы прокрутки в вертикальном направлении */
::-webkit-scrollbar-thumb {
    background-color: #9400D3; /* Цвет полосы прокрутки */
    border-radius: 10px; /* Скругление углов полосы прокрутки */
}

/* Стили для полосы прокрутки при наведении */
::-webkit-scrollbar-thumb:hover {
    background-color: #800080; /* Измененный цвет полосы прокрутки при наведении */
}

/* Стили для полосы прокрутки при активации (нажатии) */
::-webkit-scrollbar-thumb:active {
    background-color: #4B0082; /* Измененный цвет полосы прокрутки при активации */
}



</style>








<!-- Второе меню -->
<div class="second-menu">
    <div style="color: #006400; text-align: center; font-weight: bold;">Навигация</div>
    <br>
    <div style="color: #E0FFFF; text-align: center;">Игры</div>
    <br>
    <!-- Контейнер для первых трех кнопок -->
    <div style="text-align: center;">
        <button onclick="showSection1()" style="font-size: 16px; padding: 8px;">Minecraft</button>
        <button onclick="showSection2()" style="font-size: 16px; padding: 8px;">Counter Strike</button>
        <button onclick="showSection3()" style="font-size: 16px; padding: 8px;">GTA</button>
    </div>
    <!-- Конец контейнера для первых трех кнопок -->
    <br>
    <div style="color: #E0FFFF; text-align: center;">Рынок</div>
    <br>
    <button onclick="showSection04()" style="font-size: 16px; padding: 8px;">Правила</button>
    <button onclick="showSection4()" style="font-size: 16px; padding: 8px;">Аккаунты/виртуальные ресурсы онлайн игр</button>
    <button onclick="showSection5()" style="font-size: 16px; padding: 8px;">Продажа читов/софта</button>
    <br>
    <div style="color: #E0FFFF; text-align: center;">Прочее</div>
    <br>
    <button onclick="showSection6()" style="font-size: 16px; padding: 8px;">Общение</button>
    <button onclick="showSection7()" style="font-size: 16px; padding: 8px;">Обсуждение</button>
    <!-- Конец добавления -->
</div>

<div class="info-button" onclick="toggleSecond()" style="background-color: #008000; color: #E0FFFF;">Показать информацию</div>




<!-- Окно для первого раздела -->
<div class="centered-window" id="section1Window" style="height: 850px; top:65%; position: absolute; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section1Window')">✖</span>
    <!-- Содержимое для первого раздела -->
    <h2 align=center>Minecraft</h2>
    <p align=center>Категории</p>
    <!-- Добавленные красиво оформленные кнопки с нумерацией -->
    <div class="buttons">
        <!-- Передаем номер раздела в функцию -->
        <button class="styled-button button1" onclick="openNewSection(1)">Читы Minecraft</button>
        <br> <!-- Добавляем перенос строки -->
        <!-- Передаем номер раздела в функцию -->
        <button class="styled-button button2" onclick="openNewSection(2)">Модификации Minecraft</button>
        <br> <!-- Добавляем перенос строки -->
        <!-- Передаем номер раздела в функцию -->
        <button class="styled-button button3" onclick="openNewSection(3)">Разное Minecraft</button>
    </div>
</div>




<!-- Окно для второго раздела -->
<div class="centered-window" id="section2Window" style="height: 105%; top:70%; width: 50%; position: absolute; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section2Window')">✖</span>
    <!-- Содержимое для второго раздела -->
    <h2 align=center>Counter Strike</h2>
    <p align=center>Категории</p>
    <!-- Добавленные красиво оформленные кнопки с нумерацией -->
    <div class="buttons">
        <button class="styled-button button1" onclick="openNewSection(4)">Читы CS 1.6</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button button2" onclick="openNewSection(5)">Читы CSS</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button button3" onclick="openNewSection(6)">Читы CS2</button>
    </div>
</div>



<script>
    // Глобальная переменная для хранения предыдущего содержимого окна
    var previousContent = {};

    // Глобальная переменная для хранения предыдущего содержимого окна пятого раздела
    var previousFifthSectionContent = {};

    function openNewSection(sectionNumber) {
        // Получаем текущее окно в зависимости от номера раздела
        var currentWindow;
        if (sectionNumber < 4) {
            currentWindow = document.getElementById('section1Window');
        } else if (sectionNumber < 7) {
            currentWindow = document.getElementById('section2Window');
        } else if (sectionNumber < 10) {
            currentWindow = document.getElementById('section3Window');
        } else if (sectionNumber < 14) {
            currentWindow = document.getElementById('section4Window');
        } else {
            currentWindow = document.getElementById('section5Window');
        }

        // Если предыдущее содержимое для данного окна уже сохранено, восстанавливаем его
        if (previousContent[currentWindow.id]) {
            currentWindow.innerHTML = previousContent[currentWindow.id];
        }

        // Сохраняем текущее содержимое окна как предыдущее
        previousContent[currentWindow.id] = currentWindow.innerHTML;

        // Обновляем содержимое текущего окна в зависимости от номера раздела
        switch(sectionNumber) {
            case 1:
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section1Window')">✖</span>
        <h2 class="section-title">Читы Minecraft</h2>
        <div class="instructions">
            <p>1. Скачиваем архив</p>
            <p>2. Разархивировать архив</p>
            <p>3. Заходим в папку calestial и запускаем файл start.bat</p>
            <p>p.s; чтобы загрузить кфг нужно перекинуть конфиги в C:\\Celestial\\configs</p>
        </div>
        <p class="video-title">Видео рикера:</p>
        <div class="video-container">
            <iframe width="560" height="315" src="https://www.youtube.com/embed/XVUYHg1sIKI" frameborder="0" allowfullscreen></iframe>
        </div>
        <p class="download-link">Скачать файл: <a href="https://disk.yandex.ru/d/8AJorYBP8D8NWQ">Скачать CELESTIAL</a></p>
        <button class="back-button" onclick="goBack()">Назад</button>`;
                                          
                                          
                break;
               case 2:
        currentWindow.innerHTML = `
            <!-- Крестик закрытия -->
            <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section1Window')">✖</span>
            <h2 class="section-title" align=center>Модификации Minecraft</h2>
            <br>
            <div class="image-container">
                <img src="MineB.gif" style="width: 50%; height: 50%; display: block; margin: 0 auto;" alt="Изображение">
            </div>
            <br>
            <p class="link-text">Ссылка на моды: <a href="https://minecraft-inside.ru/">Нажмите здесь</a></p>
            <button class="back-button" onclick="goBack()">Назад</button>`;                                          
                                          
                break;
            case 3:
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section1Window')">✖</span>
        <h2 class="section-title" style="text-align: center;">Разное Minecraft</h2>
        <!-- Ваша информация здесь -->
        <div style="text-align: center;">
            <br>
            <img src="chicken.webp" alt="Гифка или изображение" style="width: 50%; height: auto;">
            <br>
            <br>
            <p>Перейти ➞  <a href="https://minecraft-inside.ru/crafting/#Акациевая_плита">Рецепты</a></p>
            <br>
            <p>**Причины популярности Майнкрафт**</p>
<p>Известность видеоигры легко объяснить:</p>
<ul>
    <li>**Полная свобода:** Здесь есть место для творчества и самовыражения без рамок. В период появления Майнкрафта подобных игр было очень мало, поэтому пользователи не могли не заметить такую крутую новинку.</li>
    <li>**Всё просто:** Достаточно запустить игру, и можно сразу начать строить свой мир. Интерфейс предельно понятный, ничего лишнего нет. Просто аналог конструктора, в который мы все играли в детстве.</li>
    <li>**Свой стиль:** Маркус Перссон создал «кубический» дизайн больше для собственного развлечения. Кто бы мог подумать, что именно это так зацепит пользователей. И кстати, стиль не ставит никаких ограничений — просто круглые в обычной жизни предметы здесь становятся квадратными.</li>
    <li>**Множество модов:** Они дают ещё больше свободы. Можно установить моды для красивых эффектов, добавления новых функций, оптимизации игрового процесса.</li>
    <li>**Режимы на любой вкус:** Выживание, стройка, поединки, преодоление препятствий — здесь можно делать всё, что захочется.</li>
    <li>**Нетребовательность:** Для игры подойдёт ПК с 4 ГБ оперативной памяти, процессором Intel Core i3 и видеочипом уровня Intel HD Graphics 4400. Можно создать сервер Майнкрафт и выбрать тариф с более широкими возможностями.</li>
</ul>
<p>Кстати, игра даже участвовала в благотворительных программах. Одна из них была направлена на поддержку Беловежской пущи. В Майнкрафте был создан такой же лес, а затем один из стримеров показал эту карту с вырубленными деревьями. Результат не заставил себя долго ждать: пользователи охотно пополнили фонд помощи Беловежской пуще.</p>
        </div>
        <button class="back-button" onclick="goBack()">Назад</button>`;
                break;
                
                
            case 4:
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section2Window')">✖</span>
        <h2 class="section-title" align="center">Читы CS 1.6</h2>
        <div class="gif-container">
            <!-- Вставьте сюда ссылку на вашу гифку -->
            <img src="cs16.gif" alt="Гифка" class="center-image" style="width: 35%; max-height: 30%; display: block; margin: 0 auto;">
        </div>
        <div class="features">
            <p align="center"><strong>Функции:</strong></p>
            <ul>
                <li>Visuals</li>
                <ul>
                    <li>BoxESP</li>
                    <li>BoneESP</li>
                    <li>NameESP</li>
                    <li>WeaponESP</li>
                    <li>HealthBar</li>
                    <li>SnapLine</li>
                    <li>EyeRay</li>
                    <li>Fov Line</li>
                    <li>Headshot Line</li>
                </ul>
                <li>Aimbot</li>
                <ul>
                    <li>Draw Fov</li>
                    <li>Bone</li>
                    <li>Smooth</li>
                    <li>RCS</li>
                </ul>
                <li>Radar</li>
                <ul>
                    <li>Radar Proportion</li>
                    <li>Radar Range</li>
                </ul>
                <li>Triggerbot</li>
                <ul>
                    <li>Triggerbot</li>
                    <li>Delay</li>
                    <li>HotKey</li>
                </ul>
                <li>Config</li>
                <ul>
                    <li>Create Config</li>
                    <li>Load Selected Config</li>
                    <li>Save Selected Config</li>
                    <li>Saves To Windows Documents Folder (in a folder called ".Aeonix")</li>
                    <li>Reset Config (with prompt)</li>
                    <li>Delete Config (with prompt)</li>
                    <li>Open Config Directory</li>
                </ul>
                <li>Misc</li>
                <ul>
                    <li>Triggerbot</li>
                    <li>Crosshair</li>
                    <li>Team Check</li>
                    <li>OBS Check</li>
                    <li>Visibility Check</li>
                </ul>
                <li>Window Styles</li>
                <li>Source code</li>
            </ul>
        </div>
        <div class="image-container">
            <!-- Вставьте сюда ссылку на вашу картинку -->
            <img src="cs16.png" alt="Картинка" class="center-image" style="width: 50%; height: auto;">
        </div>
        <button class="back-button" onclick="goBackSecondSection()">Назад</button>`;
                break;
                
            case 5:
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section2Window')">✖</span>
        <h2 class="section-title" align="center">Читы CSS</h2>
        <div class="gif-container">
            <!-- Вставьте сюда ссылку на вашу гифку -->
            <img src="css.gif" alt="Гифка" class="center-image" style="width: 35%; max-height: 30%; display: block; margin: 0 auto;">
        </div>
        <div class="features">
            <p align="center"><strong>Функции:</strong></p>
            <ul>
                <li>Visuals</li>
                <ul>
                    <li>BoxESP</li>
                    <li>BoneESP</li>
                    <li>SnapLine</li>
                    <li>EyeRay</li>
                    <li>Fov Line</li>
                    <li>Headshot Line</li>
                </ul>
                <li>Aimbot</li>
                <ul>
                    <li>Draw Fov</li>
                    <li>Bone</li>
                    <li>Smooth</li>
                    <li>RCS</li>
                </ul>
                <li>Radar</li>
                <ul>
                    <li>Radar Proportion</li>
                    <li>Radar Range</li>
                </ul>
                <li>Triggerbot</li>
                <ul>
                    <li>Triggerbot</li>
                </ul>
                <li>Config</li>
                <li>Misc</li>
                <ul>
                    <li>Triggerbot</li>
                    <li>Crosshair</li>
                    <li>Team Check</li>
                    <li>OBS Check</li>
                    <li>Visibility Check</li>
                </ul>
                <li>Window Styles</li>
                <li>Source code</li>
            </ul>
        </div>
        <div class="image-container">
            <!-- Вставьте сюда ссылку на вашу картинку -->
            <img src="cheatcss.jpg" alt="Картинка" class="center-image" style="width: 50%; height: auto;">
        </div>
        <button class="back-button" onclick="goBackSecondSection()">Назад</button>`;
        
                break;
            case 6:
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section2Window')">✖</span>
        <h2 class="section-title" align="center">Читы CS2</h2>
        <div class="gif-container">
            <!-- Вставьте сюда ссылку на вашу гифку -->
            <img src="cs2.gif" alt="Гифка" class="center-image" style="width: 35%; max-height: 30%; display: block; margin: 0 auto;">
        </div>
        <div class="features">
            <p align="center"><strong>Функции:</strong></p>
            <ul>
                <li>Visuals</li>
                <ul>
                    <li>BoxESP</li>
                    <li>BoneESP</li>
                    <li>NameESP</li>
                    <li>WeaponESP</li>
                    <li>HealthBar</li>
                    <li>SnapLine</li>
                    <li>EyeRay</li>
                    <li>Fov Line</li>
                    <li>Headshot Line</li>
                </ul>
                <li>Aimbot</li>
                <ul>
                    <li>Draw Fov</li>
                    <li>Bone</li>
                    <li>Smooth</li>
                    <li>RCS</li>
                </ul>
                <li>Radar</li>
                <ul>
                    <li>Radar Proportion</li>
                    <li>Radar Range</li>
                </ul>
                <li>Triggerbot</li>
                <ul>
                    <li>Triggerbot</li>
                    <li>Delay</li>
                    <li>HotKey</li>
                </ul>
                <li>Config</li>
                <ul>
                    <li>Create Config</li>
                    <li>Load Selected Config</li>
                    <li>Save Selected Config</li>
                    <li>Saves To Windows Documents Folder (in a folder called ".Aeonix")</li>
                    <li>Reset Config (with prompt)</li>
                    <li>Delete Config (with prompt)</li>
                    <li>Open Config Directory</li>
                </ul>
                <li>Misc</li>
                <ul>
                    <li>Triggerbot</li>
                    <li>Crosshair</li>
                    <li>Team Check</li>
                    <li>OBS Check</li>
                    <li>Visibility Check</li>
                </ul>
                <li>Window Styles</li>
                <li>Source code</li>
            </ul>
        </div>
        <div class="image-container">
            <!-- Вставьте сюда ссылку на вашу картинку -->
            <img src="cheatcs2.png" alt="Картинка" class="center-image" style="width: 50%; height: auto;">
        </div>
        <button class="back-button" onclick="goBackSecondSection()">Назад</button>`;
                                      
                break;
case 7: // Добавлен новый раздел о GTA
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section3Window')">✖</span>
        <h2 align=center>GTA</h2>
        <p align=center>Содержимое нового окна третьего раздела</p>
        <img src="gta5.gif" alt="Верхняя гифка" style="width: 30%; height: auto; display: block; margin: 0 auto;">
        <p>Список всех функций в билде inkabanium v0.2.</p>
        <p>Вкладка Combat:</p>
        <ul>
            <li>Aimbot (Right Mouse Button)</li>
            <li>Include peds in Aimbot check</li>
            <li>Disable weapon Spread</li>
            <li>Disable weapon Recoil</li>
            <li>Fast weapon Reload</li>
        </ul>
        <p>Вкладка Visuals:</p>
        <ul>
            <li>Draw switch (enable/disable visuals)</li>
            <li>- categories -</li>
            <li>Players</li>
            <li>Objects</li>
            <li>Vehicles</li>
            <li>Pickups</li>
        </ul>
        <p>Вкладка Self:</p>
        <ul>
            <li>Auto-Fill GodMode</li>
            <li>Health Fill</li>
            <li>Armor Fill</li>
        </ul>
        <p>Вкладка Info:</p>
        <p>Носит чисто визуальный характер, вовремя разработки использовал ее как место для вывода/отрисовки нужной информации.</p>
        <p>На релизе решил добавить в нее напоминалку и __TIMESTAMP__.</p>
        <img src="GTA5CHEAT.PNG" alt="Нижняя картинка" style="width: 50%; height: auto; display: block; margin: 0 auto;">
        <button class="back-button" onclick="goBackThirdSection()">Назад</button>`;
        
    break;
                                          
                                          
                break;
case 8: // Добавлен новый раздел о GTA  
currentWindow.innerHTML = `  
<!-- Крестик закрытия -->  
<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section3Window')">✖</span>  
<h2 align=center>GTA</h2>  
<p align=center>Содержимое нового окна третьего раздела</p>  
<img src="gta5v.gif" alt="Верхняя гифка" style="width: 30%; height: auto; display: block; margin: 0 auto;">  
<p>   </p>  
<p> <p align=center>Перейти ➞  <a href="https://www.nexusmods.com/gta5/mods/?BH=0">Моды</a></p> </p>  
<img src="gta5z.png" alt="Нижняя картинка" style="width: 70%; height: auto; display: block; margin: 0 auto;">  
<button class="back-button" onclick="goBackThirdSection()">Назад</button>`; 
        
        
                break;
                
                
            case 9: // Добавлен новый раздел о GTA  
currentWindow.innerHTML = `  
<!-- Крестик закрытия -->  
<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section3Window')">✖</span>  
<h2 align=center>GTA</h2>  
<p align=center>Содержимое нового окна третьего раздела</p>  
<img src="gta5dancer.gif" alt="Верхняя гифка" style="width: 30%; height: auto; display: block; margin: 0 auto;">  
<p>Список </p>  
<p>Установка:<br>
Распаковать архив в любую папку<br>
Открыть командную строку, прописать путь в папку с сервером и выполнить команду npm install<br>
Дождаться установки пакетов<br>
Перенести файлы сервера в вашу папку(server.exe и т.д)<br>
Данные от БД внести в packages/union-rp/modules/DB.js<br>
На ошибки при импорте бд не обращайте внимание<br>
Данные от почты gmail внести в packages/union-rp/modules/mailSender.js(При регистрации для подтверждения аккаунта)<br>
В настройках почты вы должны включить функцию "Ненадежные приложения, у которых есть доступ к аккаунту"(Необязательно)<br>
Готово<br>
Код в чат для выдачи админки: Dexh78FMM0iICE1wNHA5<br>
Консоль админов на клавишу "Ё"<br>
При запуске сервера у вас должна быть такая консоль:</p>  
<img src="console.PNG" alt="Нижняя картинка" style="width: 50%; height: auto; display: block; margin: 0 auto;">  
<button class="back-button" onclick="goBackThirdSection()">Назад</button>`; 

                break;
            case 10: // Добавляем раздел "АКВИР"
                openAKVIRSection(); // Открываем раздел "АКВИР"
                break;
            case 11: // Добавляем раздел "Cheats Minecraft"
                openCheatsMinecraftSection(); // Открываем раздел "Cheats Minecraft"
                break;
            case 12: // Добавляем раздел "Cheats CS"
                openCheatsCSSection(); // Открываем раздел "Cheats CS"
                break;
            case 13: // Добавляем раздел "Cheats GTA"
                openCheatsGTASection(); // Открываем раздел "Cheats GTA"
                break;
            case 14: // Добавляем раздел "Software"
                openSoftwareSection(); // Открываем раздел "Software"
                break;
        }
    }

    // Функция для возврата к предыдущему содержимому окна первого раздела
    function goBack() {
        var currentWindow = document.getElementById('section1Window');
        currentWindow.innerHTML = previousContent[currentWindow.id];
    }

    // Функция для возврата к предыдущему содержимому окна второго раздела
    function goBackSecondSection() {
        var currentWindow = document.getElementById('section2Window');
        currentWindow.innerHTML = previousContent[currentWindow.id];
    }

    // Функция для возврата к предыдущему содержимому окна третьего раздела
    function goBackThirdSection() {
        var currentWindow = document.getElementById('section3Window');
        currentWindow.innerHTML = previousContent[currentWindow.id];
    }

    // Функция для возврата к предыдущему содержимому окна пятого раздела
    function goBackFifthSection() {
        var currentWindow = document.getElementById('section5Window');
        currentWindow.innerHTML = previousFifthSectionContent[currentWindow.id];
    }

    // Функция для открытия раздела "АКВИР"
    function openAKVIRSection() {
        var currentWindow = document.getElementById('section4Window');
        // Сохраняем предыдущее содержимое окна АКВИР
        previousContent[currentWindow.id] = currentWindow.innerHTML;
        currentWindow.innerHTML = '<!-- Крестик закрытия -->' +
                                  '<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection(\'section4Window\')">✖</span>' +
                                  '<h2>АКВИР</h2>' +
                                  '<p>Выберите категорию:</p>' +
                                  '<div class="buttons">' +
                                  '<button class="styled-button" onclick="openAccountsSection()">Аккаунты</button><br>' +
                                  '<button class="styled-button second-button" onclick="openVirtsSection()">Вирты</button>' +
                                  '</div>';
    }

    // Функция для открытия подраздела "Аккаунты" в разделе "АКВИР"
function openAccountsSection() {
    var currentWindow = document.getElementById('section4Window');
    // Сохраняем предыдущее содержимое окна АКВИР
    previousContent[currentWindow.id] = currentWindow.innerHTML;
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section4Window')">✖</span>
        <img src="33.gif" alt="Верхняя гифка" style="width: 10%; height: auto; display: block; margin: 0 auto;">
        <h2>Аккаунты</h2>
        <p>Содержимое раздела "Аккаунты"</p>
        <button class="back-button" onclick="goBackAKVIR()">Назад</button>`; // Добавляем обработчик событий для кнопки "Назад"
}

    // Функция для открытия подраздела "Вирты" в разделе "АКВИР"
function openVirtsSection() {
    var currentWindow = document.getElementById('section4Window');
    // Сохраняем предыдущее содержимое окна АКВИР
    previousContent[currentWindow.id] = currentWindow.innerHTML;
    currentWindow.innerHTML = `
        <!-- Крестик закрытия -->
        <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section4Window')">✖</span>
        <img src="smoney.gif" alt="Верхняя гифка" style="width: 30%; height: auto; display: block; margin: 0 auto;">
        <h2>Вирты</h2>
        <p>Содержимое раздела "Вирты"</p>
        <button class="back-button" onclick="goBackAKVIR()">Назад</button>`; // Добавляем обработчик событий для кнопки "Назад"
      }

    // Функция для возврата к разделу "АКВИР"
    function goBackAKVIR() {
        var currentWindow = document.getElementById('section4Window');
        // Возвращаем предыдущее содержимое окна АКВИР
        currentWindow.innerHTML = previousContent[currentWindow.id];
    }

    // Функция для открытия раздела "Cheats Minecraft"
    function openCheatsMinecraftSection() {
        var currentWindow = document.getElementById('section5Window');
        // Сохраняем предыдущее содержимое окна пятого раздела
        previousFifthSectionContent[currentWindow.id] = currentWindow.innerHTML;
        currentWindow.innerHTML = '<!-- Крестик закрытия -->' +
                                  '<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection(\'section5Window\')">✖</span>' +
                                  '<h2>Читы Minecraft</h2>' +
                                  '<p>Содержимое раздела "Cheats Minecraft"</p>' +
                                  '<button class="back-button" onclick="goBackFifthSection()">Назад</button>'; // Добавляем кнопку "Назад"
    }

    // Функция для открытия раздела "Cheats CS"
    function openCheatsCSSection() {
        var currentWindow = document.getElementById('section5Window');
        // Сохраняем предыдущее содержимое окна пятого раздела
        previousFifthSectionContent[currentWindow.id] = currentWindow.innerHTML;
        currentWindow.innerHTML = '<!-- Крестик закрытия -->' +
                                  '<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection(\'section5Window\')">✖</span>' +
                                  '<h2>Читы CS</h2>' +
                                  '<p>Содержимое раздела "Cheats CS"</p>' +
                                  '<button class="back-button" onclick="goBackFifthSection()">Назад</button>'; // Добавляем кнопку "Назад"
    }

    // Функция для открытия раздела "Cheats GTA"
    function openCheatsGTASection() {
        var currentWindow = document.getElementById('section5Window');
        // Сохраняем предыдущее содержимое окна пятого раздела
        previousFifthSectionContent[currentWindow.id] = currentWindow.innerHTML;
        currentWindow.innerHTML = '<!-- Крестик закрытия -->' +
                                  '<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection(\'section5Window\')">✖</span>' +
                                  '<h2>Читы GTA</h2>' +
                                  '<p>Содержимое раздела "Cheats GTA"</p>' +
                                  '<button class="back-button" onclick="goBackFifthSection()">Назад</button>'; // Добавляем кнопку "Назад"
    }

    // Функция для открытия раздела "Software"
    function openSoftwareSection() {
        var currentWindow = document.getElementById('section5Window');
        // Сохраняем предыдущее содержимое окна пятого раздела
        previousFifthSectionContent[currentWindow.id] = currentWindow.innerHTML;
        currentWindow.innerHTML = '<!-- Крестик закрытия -->' +
                                  '<span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection(\'section5Window\')">✖</span>' +
                                  '<h2>Софт</h2>' +
                                  '<p>Содержимое раздела "Software"</p>' +
                                  '<button class="back-button" onclick="goBackFifthSection()">Назад</button>'; // Добавляем кнопку "Назад"
    }
</script>







<!-- Окно для третьего раздела -->
<div class="centered-window" id="section3Window" style="height: 750px; top:65%; position: absolute; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section3Window')">✖</span>
    <!-- Содержимое для третьего раздела -->
    <h2 align=center>Grand Theft Auto</h2>
    <p align=center>Категории</p>
    <!-- Добавленные красиво оформленные кнопки с нумерацией -->
    <div class="buttons">
        <button class="styled-button button1" onclick="openNewSection(7)">Читы GTA</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button button2" onclick="openNewSection(8)">Модификации для GTA</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button button3" onclick="openNewSection(9)">Разное GTA</button>
    </div>
</div>

<style>
/* Стили для кнопок в 3 окне */


#section5Window .buttons button {
    padding: 10px 20px; /* Задаем отступы для кнопок */
    margin: 5px; /* Задаем внешний отступ между кнопками */
    border: none; /* Убираем границу кнопок */
    border-radius: 5px; /* Задаем скругление углов кнопок */
    background-color: #4CAF50; /* Цвет фона кнопок */
    color: white; /* Цвет текста кнопок */
    font-size: 16px; /* Размер шрифта кнопок */
    cursor: pointer; /* Задаем указатель при наведении на кнопки */
}

#section5Window .buttons button:hover {
    background-color: #45a049; /* Изменяем цвет фона кнопок при наведении */
}

/* Стили для каждой отдельной кнопки */
.button1 {
    background-color: #4CAF50; /* Зеленый цвет */
    border: none;
    color: white;
    padding: 5px 90px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
}

.button2 {
    background-color: #33aaff; /* Цвет фона для второй кнопки */
    /* Дополнительные стили для второй кнопки */
}

.button3 {
    background-color: #ff33aa; /* Цвет фона для третьей кнопки */
    /* Дополнительные стили для третьей кнопки */
}

.button4 {
    background-color: #33ff57; /* Цвет фона для четвертой кнопки */
    /* Дополнительные стили для четвертой кнопки */
}
</style>







<!-- Окно для раздела 04 -->
<div class="centered-window" id="section04Window" style="height: 900px; top: 600px; position: absolute; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section04Window')">✖</span>
    <!-- Содержимое для раздела 04 -->
   
    <br>
    
<title>Правила виртуального рынка на LolNet</title>
<style>
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0; /* изменено на 0 */
}
  h1 {
    text-align: center;
    color: #333;
  }
  h2 {
    color: #333;
  }
  p {
    margin-bottom: 20px;
  }
  ul {
    margin-bottom: 20px;
    padding-left: 20px;
  }
</style>
</head>
<body>
<h1>Правила виртуального рынка на <font color="green" face="Mv boli" size="15px">L</font><font color="#808000" face="Mv boli" size="5px">oLNet</font></h1>
<br>

<p>Виртуальный рынок - место для обмена виртуальным имуществом пользователей сайта <font color="green" face="Mv boli" size="15px">L</font><font color="#808000" face="Mv boli" size="5px">oLNet</font>. Здесь совершается обмен/купля/продажа аккаунтов и валюты с минимальными для вас рисками.</p>

<h2>Правила рынка:</h2>
<ul>
  <li>Все сделки в этом разделе регламентируются действующими правилами сайта, а также правилами отдельно взятого раздела "Рынок".</li>
  <li>Запрещено обманывать пользователей и нарушать правила раздела.</li>
  <li>Запрещено вымогательство имущества у продавцов и покупателей.</li>
  <li>Запрещена выдача себя за гаранта или администратора для проведения сделок.</li>
</ul>

<p>Тема оформляется по форме:</p>
<ol>
  <li>Товар (пример: вирты/аккаунт)</li>
  <li>Желаемая сумма и метод оплаты (купля/продажа)</li>
  <li>Описание (если не валюта)</li>
  <li>Как с вами связаться (ЛС на сайте/профиль в мессенджере)</li>
</ol>

<p>Сумма за товар устанавливается вами и не подлежит изменению никем другим.</p>

<p>Администрация сайта имеет право закрыть вашу тему, если она не удовлетворяет требованиям данных правил или автор нарушил пользовательское соглашение и правила сайта.</p>

<p>Если один из участников сделки захотел воспользоваться услугами гаранта и сам желает их оплатить, то вы не имеете права ему отказывать. Если оплатить гаранта просят вас - право наёма остаётся за вами.</p>

<p>Ап своих тем разрешен не чаще, чем 1 раз в 24 часа.</p>

<p>При создании темы в разделе "Продажа читов/софта" необходимо добавить демонстрацию работоспособности софта.</p>

<p>В обсуждении предложения на рынке запрещено безосновательно оставлять осуждающие либо хвалебные отзывы.</p>

<p>К продаже не допускаются стиллеры, лоадеры, ратники, а также сервисы, предоставляющие такого рода товары.</p>

<h2>Ограничения для размещения объявлений, к которым причастны забаненные на форуме пользователи:</h2>
<ul>
  <li>Не допускаются любые объявления с предложением/запросом услуг и товаров, если кто-то из участников сделки имеет действующий бан за мошенничество.</li>
  <li>Не допускаются объявления о продаже софта, если любой представитель организации, ответственной за этот софт, имеет действующий бан за распространение вредоносного ПО.</li>
  <li>Другие объявления о сделках, совершаемых при участии навсегда заблокированного пользователя, отмечаются тревожным предупреждением.</li>
</ul>

<h2>Тематика раздела "Рынок":</h2>
<p>Темы раздела "Рынок" ограничиваются следующими пунктами:</p>
<ul>
  <li>Продажа/покупка/обмен игровых аккаунтов и внутриигровых ценностей</li>
  <li>Продажа приватного софта для игр (читы, помощники и т.д.)</li>
  <li>Заказы/предложения об услугах разработки (программирование), создания дизайна, прокачки игровых аккаунтов</li>
  <li>Специализированные прокси/VPN для игр или софта для игр.</li>
</ul>

<p>Все темы, не попадающие под вышеуказанные тематики, не будут допущены к публикации, однако список может быть расширен, а также из него могут быть сделаны исключения на усмотрение модерации.</div>



<!-- Окно для раздела "АКВИР" -->
<div class="centered-window" id="section4Window" style="position: absolute; height: 400px; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section4Window')">✖</span>
    <!-- Содержимое для раздела "Аккаунты/Вирты" -->
    <h2>Аккаунты/Вирты</h2>
    <p>Выберите категорию:</p>
    <!-- Кнопки для выбора категории -->
    <div class="buttons">
        <button class="styled-button" onclick="openAccountsSection()">Аккаунты</button>
        <br> <!-- Перенос строки -->
        <button class="styled-button second-button" onclick="openVirtsSection()">Вирты</button>
    </div>
</div>







<style>
.styled-button {
    background-color: #4CAF50; /* Зеленый цвет */
    border: none;
    color: white;
    padding: 5px 90px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
}

.styled-button:hover {
    background-color: #45a049; /* Темнозеленый цвет при наведении */
}

.second-button {
    background-color: #f44336; /* Красный цвет */
    border: none;
    color: white;
    padding: 5px 100px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;

}

.second-button:hover {
    background-color: #d32f2f; /* Темно-красный цвет при наведении */
}


</style>









<!-- Окно для пятого раздела -->
<div class="centered-window" id="section5Window" style="position: absolute; height: 400px; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section5Window')">✖</span>
    <!-- Содержимое для пятого раздела -->
    <h2>СОФТ</h2>
    <p>Категории</p>
    <!-- Добавленные красиво оформленные кнопки с нумерацией -->
    <div class="buttons">
        <button class="styled-button" onclick="openNewSection(11)">Cheats Minecraft</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button" onclick="openNewSection(12)">Cheats CS</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button" onclick="openNewSection(13)">Cheats GTA</button>
        <br> <!-- Добавляем перенос строки -->
        <button class="styled-button" onclick="openNewSection(14)">Software</button>
    </div>
</div>

<style>
/* Стили для кнопок в пятом окне */


#section5Window .buttons button {
    padding: 10px 20px; /* Задаем отступы для кнопок */
    margin: 5px; /* Задаем внешний отступ между кнопками */
    border: none; /* Убираем границу кнопок */
    border-radius: 5px; /* Задаем скругление углов кнопок */
    background-color: #4CAF50; /* Цвет фона кнопок */
    color: white; /* Цвет текста кнопок */
    font-size: 16px; /* Размер шрифта кнопок */
    cursor: pointer; /* Задаем указатель при наведении на кнопки */
}

#section5Window .buttons button:hover {
    background-color: #45a049; /* Изменяем цвет фона кнопок при наведении */
}

/* Стили для каждой отдельной кнопки */
.button1 {
    background-color: #4CAF50; /* Зеленый цвет */
    border: none;
    color: white;
    padding: 5px 90px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 10px;
}

.button2 {
    background-color: #33aaff; /* Цвет фона для второй кнопки */
    /* Дополнительные стили для второй кнопки */
}

.button3 {
    background-color: #ff33aa; /* Цвет фона для третьей кнопки */
    /* Дополнительные стили для третьей кнопки */
}

.button4 {
    background-color: #33ff57; /* Цвет фона для четвертой кнопки */
    /* Дополнительные стили для четвертой кнопки */
}
</style>













<!-- Стили для чата -->
    <style>
        /* Стили для чата */
        /* Стили для области сообщений */
        #chatMessages {
            max-height: 300px;
            overflow-y: auto;
            padding: 10px;
        }

        /* Стили для отдельного сообщения */
        .message {
            margin-bottom: 10px;
            padding: 10px;
            border-radius: 10px;
            background-color: rgba(242, 242, 242, 0.9); /* Прозрачный цвет фона */
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }

        /* Стили для логина пользователя */
        .message .login {
            font-weight: bold;
            color: #333;
            margin-bottom: 5px;
        }

        /* Стили для текста сообщения */
        .message .text {
            color: #333;
        }

        /* Стили для поля ввода сообщения */
        #messageInput {
            width: calc(100% - 120px);
            padding: 12px;
            border: none;
            border-radius: 20px;
            background-color: rgba(255, 255, 255, 0.9); /* Прозрачный белый фон */
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            font-size: 16px;
            color: #333;
        }

        /* Стили для кнопки отправки сообщения */
        #sendButton {
            width: 100px;
            padding: 12px;
            border: none;
            border-radius: 20px;
            background-color: #4CAF50;
            color: white;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        /* Стили для кнопки отправки сообщения при наведении */
        #sendButton:hover {
            background-color: #45a049;
        }

        /* Стили для кнопки закрытия окна */
        .close-button {
            position: absolute;
            top: 10px;
            right: 10px;
            cursor: pointer;
            font-size: 18px;
            color: #333; /* Черный цвет для крестика */
        }
    </style>
<!-- Окно для раздела 6 -->
<div class="centered-window" id="section6Window" style="height: 400px; position: absolute; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section6Window')">✖</span>
    <!-- Содержимое для раздела 6 -->
    <div style="padding: 10px;">
        <h2 align=center style="margin-bottom: 20px;">Чат</h2>
        <!-- Место для отображения сообщений -->
        <div id="chatMessages"></div>
        <!-- Форма ввода сообщения -->
        <input type="text" id="messageInput" style="width: calc(100% - 100px); padding: 5px; border-radius: 5px 0 0 5px; border: 1px solid #ccc;">
        <button onclick="sendMessage()" style="padding: 5px 10px; border: none; background-color: #4CAF50; color: white; border-radius: 0 5px 5px 0;">Отправить</button>
    </div>
</div>

<script>
    // Функция для отправки сообщения
    function sendMessage() {
        // Получаем значение введенного сообщения
        var message = document.getElementById("messageInput").value;

        // Получаем логин из локального хранилища
        var login = localStorage.getItem("login");

        // Если сообщение не пустое
        if (message.trim() !== "") {
            // Создаем элемент для отображения сообщения
            var messageElement = document.createElement("div");
            messageElement.className = "message";

            // Создаем элемент для отображения логина
            var loginSpan = document.createElement("span");
            loginSpan.textContent = login + ": ";
            messageElement.appendChild(loginSpan);

            // Создаем элемент для отображения текста сообщения
            var textSpan = document.createElement("span");
            textSpan.textContent = message;
            messageElement.appendChild(textSpan);

            // Добавляем сообщение в область сообщений
            document.getElementById("chatMessages").appendChild(messageElement);

            // Очищаем поле ввода
            document.getElementById("messageInput").value = "";
        }
    }
</script>




<!-- Окно для раздела 7 -->
<div class="centered-window" id="section7Window" style="position: fixed; height: 900px; position: absolute; top: 600px; overflow: auto;">
    <!-- Крестик закрытия -->
    <span class="close-button" style="position: absolute; top: 10px; right: 10px;" onclick="closeSection('section7Window')">✖</span>
    <!-- Содержимое для раздела 7 -->
    <h2>Окно по середине</h2>
    <p>Очень длинный текст, который занимает много места...</p>
</div>



<!-- JavaScript для функциональности закрытия окон -->
<script>
    function closeSection(sectionId) {
        var section = document.getElementById(sectionId);
        section.style.display = "none";
    }
</script>



<!-- JavaScript код -->
<script>
    // Функция для переключения отображения второго меню
    function toggleSecond() {
        var secondMenu = document.querySelector('.second-menu');
        if (secondMenu.style.display === 'block') {
            secondMenu.style.display = 'none';
        } else {
            secondMenu.style.display = 'block';
        }
    }

    // Функция для отображения информации о выбранном разделе
    function showInfo(info) {
        alert('Вы выбрали: ' + info);
    }

    // Функция для скрытия всех разделов
    function hideAllSections() {
        var allSections = document.querySelectorAll('.centered-window');
        allSections.forEach(function(section) {
            section.style.display = 'none';
        });
    }

    // Функции для отображения содержимого окон для каждого раздела
    function showSection1() {
        hideAllSections(); // Скрыть все разделы перед открытием нового
        var section1Window = document.getElementById('section1Window');
        section1Window.style.display = 'block';
    }

    function showSection2() {
        hideAllSections();
        var section2Window = document.getElementById('section2Window');
        section2Window.style.display = 'block';
    }

    function showSection3() {
        hideAllSections();
        var section3Window = document.getElementById('section3Window');
        section3Window.style.display = 'block';
    }

    

    function showSection04() {
        hideAllSections();
        var section04Window = document.getElementById('section04Window');
        section04Window.style.display = 'block';
    }


    function showSection4() {
        hideAllSections();
        var section4Window = document.getElementById('section4Window');
        section4Window.style.display = 'block';
    }

    function showSection5() {
        hideAllSections();
        var section5Window = document.getElementById('section5Window');
        section5Window.style.display = 'block';
    }

    function showSection6() {
        hideAllSections();
        var section6Window = document.getElementById('section6Window');
        section6Window.style.display = 'block';
    }

    function showSection7() {
        hideAllSections();
        var section7Window = document.getElementById('section7Window');
        section7Window.style.display = 'block';
    }
    
    function showSection(sectionId) {
    // Скрыть все окна
    var windows = document.getElementsByClassName("centered-window");
    for (var i = 0; i < windows.length; i++) {
        windows[i].style.display = "none";
    }
    // Показать нужное окно
    var section = document.getElementById(sectionId);
    if (section) {
        section.style.display = "block";
    }
}

function closeSection(sectionId) {
    // Скрыть окно
    var section = document.getElementById(sectionId);
    if (section) {
        section.style.display = "none";
    }
}

</script>

<footer class="footer">
<h1 align="center"><font color="green" face="Mv boli" size="5px">L</font> <font color="#B0E0E6" face="Mv boli" size="5px">oLNet</font></h1>            
<p>Created by Nikita Sergeev</p>
        </div>
    </div>
</footer>




</body>
</html>


