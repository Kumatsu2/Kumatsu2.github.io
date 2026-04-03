# Kumatsu2.github.io
happy birthday card
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>С Днём Рождения, Даша!</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Общие стили для страницы */
        body {
            font-family: 'Montserrat', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f06b6b 0%, #ffc0cb 100%); /* Нежный градиент */
            color: #333;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            overflow-x: hidden;
            text-align: center;
        }

        .container {
            width: 90%;
            max-width: 800px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            padding: 30px;
            margin: 20px 0;
            box-sizing: border-box;
        }

        h1 {
            color: #d12c2c; /* Яркий красный */
            font-size: 3em;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .subtitle {
            font-size: 1.2em;
            color: #555;
            margin-bottom: 30px;
        }

        /* Стили для плашек */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .card {
            background-color: #fff;
            border-radius: 15px;
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
            padding: 25px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: left;
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }

        .card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.2);
        }

        .card h2 {
            color: #d12c2c;
            font-size: 1.5em;
            margin-top: 0;
            margin-bottom: 15px;
            text-align: center;
        }
                .card p {
            font-size: 1em;
            line-height: 1.6;
            color: #666;
            text-align: center;
        }
        
        
        .modal {
            display: none; 
            position: fixed; 
            z-index: 1000; 
            left: 0;
            top: 0;
            width: 100%; 
            height: 100%; 
            overflow: auto; 
            background-color: rgba(0, 0, 0, 0.6); 
            backdrop-filter: blur(5px); 
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            background-color: #fff;
            margin: auto;
            padding: 30px;
            border-radius: 15px;
            width: 80%;
            max-width: 600px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            position: relative;
            animation-name: animatetop;
            animation-duration: 0.4s;
            color: #333;
            text-align: left;
        }
        
        .modal-content h3 {
            color: #d12c2c;
            margin-top: 0;
            font-size: 1.8em;
            text-align: center;
            margin-bottom: 20px;
        }
        
        .modal-content p {
            font-size: 1.1em;
            line-height: 1.8;
            margin-bottom: 15px;
            color: #555;
        }

        .close-button {
            color: #aaa;
            position: absolute;
            top: 15px;
            right: 25px;
            font-size: 35px;
            font-weight: bold;
            cursor: pointer;
            transition: color 0.3s ease;
        }

        .close-button:hover,
        .close-button:focus {
            color: #d12c2c;
            text-decoration: none;
        }

        @keyframes animatetop {
            from {top: -300px; opacity: 0} 
            to {top: 0; opacity: 1}
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>С Днём Рождения, Даша!</h1>
        <p class="subtitle">От всего нашего милого женского коллектива желаем тебе счастья, успехов и вдохновения!</p>

        <div class="card-grid">
            <!-- Плашка 1 -->
            <div class="card" onclick="openModal('modal1')">
                <h2>Наши пожелания</h2>
                <p>Кликните, чтобы прочитать самые теплые слова!</p>
            </div>

            <!-- Плашка 2 -->
            <div class="card" onclick="openModal('modal2')">
                <h2>Твои достижения</h2>
                <p>Вспомним яркие моменты уходящего года!</p>
            </div>

            <!-- Плашка 3 -->
            <div class="card" onclick="openModal('modal3')">
                <h2>Позитив и смех</h2>
                <p>Улыбнись вместе с нами!</p>
            </div>
            
            <!-- Нужны ли еще плашки? -->
            <!-- <div class="card" onclick="openModal('modal4')">
                <h2>моя команда</h2>
                <p>Кликни, чтобы узнать, что мы о тебе думаем!</p>
            </div> -->
        </div>
    </div>

    <!-- Модальное окно 1: Наши пожелания -->
    <div id="modal1" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('modal1')">&times;</span>
            <h3>Самые добрые пожелания!</h3>
            <p>Дорогая Даша, от всего сердца поздравляем тебя с Днём Рождения! Желаем крепкого здоровья, неиссякаемой энергии, больших успехов в работе и личной жизни. Пусть каждый день приносит новые радости, а вдохновение никогда не покидает!</p>
            <p>Пусть все твои планы и мечты сбываются, а каждый новый проект будет еще успешнее предыдущего. Ты невероятная подруга, и мы очень ценим твою доброту и поддержку.</p>
        </div>
    </div>

    <!-- Модальное окно 2: Твои достижения -->
    <div id="modal2" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('modal2')">&times;</span>
            <h3>Гордимся твоими успехами!</h3>
            <p>Даша, мы восхищаемся твоей способностью достигать целей и вдохновлять нас. В этом году "Лиля, скажи что она сделала. может ты знаешь"</p>
            <p>И тут еще текст</p>
        </div>
    </div>

    <!-- Модальное окно 3: Позитив и смех -->
    <div id="modal3" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('modal3')">&times;</span>
            <h3>Для хорошего настроения!</h3>
            <p>Желаем тебе, Даша, чтобы каждый твой день был наполнен улыбками, приятными сюрпризами и искренним смехом. Пусть рабочие моменты приносят только удовлетворение, а дома всегда царит тепло и уют!</p>
            <p>Помни, что каждый день — это повод для радости и новых открытий. Цени каждое мгновение и будь счастлива!</p>
        </div>
    </div>
    
    <!-- Добавьте модальные окна для новых плашек -->
    <!-- <div id="modal4" class="modal">
        <div class="modal-content">
            <span class="close-button" onclick="closeModal('modal4')">&times;</span>
            <h3>Твои подруги</h3>
            <p>Мы любим тебя, Даша!</p>
        </div>
    </div> -->

            <script>
        // Получаем все модальные окна и кнопки закрытия
        const modals = document.querySelectorAll('.modal');
        const closeButtons = document.querySelectorAll('.close-button');
        const modalBackdrops = document.querySelectorAll('.modal'); // Крестик тоже является частью modal-content, поэтому кликаем по фону modal

        // Функция для открытия модального окна
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.style.display = 'flex';
                document.body.classList.add('modal-open');
            }
        }

        // Функция для закрытия модального окна
        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            if (modal) {
                modal.style.display = 'none';
                document.body.classList.remove('modal-open');
            }
        }

        // Обработчик клика по крестикам
        closeButtons.forEach(button => {
            button.addEventListener('click', function(event) {
                event.stopPropagation(); // Предотвращаем всплытие события
                const modalId = this.parentElement.parentElement.id; // Получаем ID родительского модального окна
                closeModal(modalId);
            });
        });

        // Обработчик клика по фону модального окна
        modalBackdrops.forEach(modal => {
            modal.addEventListener('click', function(event) {
                // Проверяем, кликнули ли мы именно по фону модального окна, а не по его содержимому
                if (event.target === this) { // event.target - это элемент, по которому кликнули
                    closeModal(this.id);
                }
            });
        });
        
        // Важно: для мобильных устройств, где может быть не всегда срабатывает onclick
        // Добавляем обработчик для touchstart (аналог клика на касании)
        document.addEventListener('touchstart', function(event) {
            // Если касание было по крестику
            if (event.target.classList.contains('close-button')) {
                event.preventDefault(); // Предотвращаем стандартное поведение касания
                const modalId = event.target.parentElement.parentElement.id;
                closeModal(modalId);
                return;
            }
            // Если касание было по фону модального окна
            if (event.target.classList.contains('modal')) {
                event.preventDefault(); // Предотвращаем стандартное поведение касания
                closeModal(event.target.id);
            }
        }, { passive: false }); // passive: false нужен, чтобы preventDefault() сработал

        // Удаляем глобальный window.onclick, чтобы он не конфликтовал
        // window.onclick = null; // Можно удалить, но лучше оставить проверку в обработчиках ниже
    </script>
</body>
</html>
