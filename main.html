<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Аналог Citizen</title>

    <!-- Подключаем Leaflet из CDN -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />

    <style>
        /* Делаем карту на весь экран */
        html, body {
            height: 100%;
            margin: 0;
            padding: 0;
        }
        #map {
            width: 100%;
            height: 100%;
        }

        /* --- НОВОЕ: Скрываем стандартную атрибуцию Leaflet (флаг) --- */
        .leaflet-control-attribution {
            display: none;
        }

        /* Стиль для всплывающих окон */
        .leaflet-popup-content-wrapper {
            padding: 15px;
            font-family: Arial, sans-serif;
        }

        /* --- НОВОЕ: Стиль для нашей текстовой ссылки --- */
        .osm-attribution {
            position: absolute;
            bottom: 10px; 
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(255, 255, 255, 0.8); 
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 12px;
            z-index: 1000; 
        }

        /* Темная тема маркеров и окружностей */
        .leaflet-default-icon-path {
            background-color: #000; /* Черный маркер */
        }

        .leaflet-circle {
            stroke: red !important;
            fill-opacity: 0.3 !important;
        }
    </style>
</head>
<body>

<div id="map"></div>

<!-- Добавляем нашу собственную ссылку на OpenStreetMap -->
<div class="osm-attribution">
     <a href="www.example.com" target="_blank">Соглашение</a>
</div>

<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>
<script>
    function openExternalLink(url) { /* Кнопка откроет новую вкладку */
        window.open(url, '_blank');
    }

    // --- Инициализация карты ---
  const map = L.map('map').setView([58.311389, 82.902688], 13);
// Москва

    // Темный тайлсет
    L.tileLayer(
        'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
        {
            attribution: '© <a href="https://www.openstreetmap.org/">OpenStreetMap</a>'
        }
    ).addTo(map);

    // --- Загрузка данных из файла points.json ---
    fetch('https://raw.githubusercontent.com/andreikadudov-a11y/base-ss/refs/heads/main/points.json')
        .then(response => response.json())
        .then(data => {
            if (!Array.isArray(data)) {
                console.error("Данные из файла не являются массивом");
                return;
            }

            data.forEach(incident => {
                const coords = [incident.lat, incident.lon];

                // Создаем маркер (точку)
                const marker = L.marker(coords).addTo(map);

                // 📢 Поп-ап с кнопкой «Источник»
                marker.bindPopup(`
                    <strong>${incident.title}</strong><br>
                    ${incident.description}<br>
                    <button onclick="openExternalLink('${incident.source}')">Источник</button>
                `);

                // Красная зона вокруг инцидента
                const circle = L.circle(coords, {
                    color: 'red',
                    fillColor: '#f03',
                    fillOpacity: 0.3,
                    radius: incident.radius
                }).addTo(map);
            });

            console.log("Данные загружены и нанесены на карту", data);
        })
        .catch(error => {
            console.error("Ошибка при загрузке данных:", error);
            alert("Не удалось загрузить данные о происшествиях.");
        });
</script>
</body>
</html>
