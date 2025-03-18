<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>World War II Map Animation</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        axis: '#940000',
                        allies: '#004b87',
                        neutral: '#808080',
                        japan: '#BC002D',
                        italy: '#008C45',
                        ussr: '#CC0000',
                        usa: '#3C3B6E',
                        uk: '#00247D',
                        france: '#002654',
                        germany: '#444444'
                    }
                }
            }
        }
    </script>
    <style>
        .map-container {
            overflow: hidden;
            position: relative;
        }
        .country {
            fill: #e5e5e5;
            stroke: #fff;
            stroke-width: 0.5;
            transition: fill 0.5s ease;
        }
        .country:hover {
            stroke-width: 1;
            stroke: #000;
        }
        .dark .country {
            fill: #555;
            stroke: #333;
        }
        .dark .country:hover {
            stroke: #ccc;
        }
        .timeline-marker {
            position: absolute;
            width: 16px;
            height: 16px;
            border-radius: 50%;
            background-color: #5D5CDE;
            top: 50%;
            transform: translate(-50%, -50%);
            cursor: pointer;
            z-index: 10;
        }
        .timeline-track {
            position: relative;
            height: 4px;
            background-color: #e5e5e5;
            border-radius: 2px;
        }
        .dark .timeline-track {
            background-color: #555;
        }
        .timeline-progress {
            position: absolute;
            height: 100%;
            background-color: #5D5CDE;
            border-radius: 2px;
        }
        /* Light/Dark mode transition */
        * {
            transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
        }
        .event-container {
            max-height: 300px;
            overflow-y: auto;
        }
    </style>
</head>
<body class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 min-h-screen">
    <div class="container mx-auto px-4 py-8 max-w-6xl">
        <header class="mb-6">
            <h1 class="text-3xl font-bold text-center">World War II Territorial Changes</h1>
            <p class="text-center text-gray-600 dark:text-gray-400 mt-2">1939-1945</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
            <div class="lg:col-span-2 bg-white dark:bg-gray-800 rounded-lg shadow-md p-4">
                <div class="map-container aspect-[4/3] bg-blue-50 dark:bg-gray-700 rounded-lg">
                    <svg id="world-map" width="100%" height="100%" viewBox="0 0 1000 600" preserveAspectRatio="xMidYMid meet">
                        <g id="map-group"></g>
                        <g id="labels"></g>
                    </svg>
                </div>

                <div class="mt-6 px-2">
                    <div class="flex items-center justify-between mb-2">
                        <button id="play-pause" class="bg-primary hover:bg-opacity-80 text-white px-4 py-2 rounded-lg flex items-center">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-1" viewBox="0 0 20 20" fill="currentColor">
                                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd" />
                            </svg>
                            <span>Play</span>
                        </button>
                        <span id="date-display" class="font-bold text-xl">September 1939</span>
                        <button id="reset" class="bg-gray-200 dark:bg-gray-700 hover:bg-gray-300 dark:hover:bg-gray-600 px-4 py-2 rounded-lg">
                            Reset
                        </button>
                    </div>
                    <div class="relative py-4">
                        <div class="timeline-track">
                            <div id="timeline-progress" class="timeline-progress" style="width: 0%"></div>
                        </div>
                        <div id="timeline-marker" class="timeline-marker" style="left: 0%"></div>
                        <div class="flex justify-between mt-2 text-sm">
                            <span>1939</span>
                            <span>1940</span>
                            <span>1941</span>
                            <span>1942</span>
                            <span>1943</span>
                            <span>1944</span>
                            <span>1945</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="bg-white dark:bg-gray-800 rounded-lg shadow-md p-4">
                <h2 class="text-xl font-bold mb-4">Powers & Key Events</h2>
                
                <div class="mb-6">
                    <h3 class="font-bold mb-2">Legend</h3>
                    <div class="grid grid-cols-2 gap-2">
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-axis mr-2"></div>
                            <span>Nazi Germany</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-italy mr-2"></div>
                            <span>Italy</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-japan mr-2"></div>
                            <span>Japan</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-uk mr-2"></div>
                            <span>United Kingdom</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-france mr-2"></div>
                            <span>France</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-ussr mr-2"></div>
                            <span>USSR</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-usa mr-2"></div>
                            <span>USA</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-4 h-4 bg-neutral mr-2"></div>
                            <span>Neutral</span>
                        </div>
                    </div>
                </div>
                
                <div>
                    <h3 class="font-bold mb-2">Current Events</h3>
                    <div id="event-info" class="event-container prose dark:prose-invert prose-sm max-w-none">
                        <p>Move the timeline or click play to see events.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Check for dark mode preference
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            if (event.matches) {
                document.documentElement.classList.add('dark');
            } else {
                document.documentElement.classList.remove('dark');
            }
        });

        // Simplified world map data - just enough countries to illustrate WW2
        const mapData = {
            "type": "FeatureCollection",
            "features": [
                { "type": "Feature", "id": "DEU", "properties": { "name": "Germany" }, "geometry": { "type": "Polygon", "coordinates": [[[9, 53], [13, 53], [14, 51], [12, 48], [9, 48], [7, 49], [6, 51], [9, 53]]] } },
                { "type": "Feature", "id": "POL", "properties": { "name": "Poland" }, "geometry": { "type": "Polygon", "coordinates": [[[15, 54], [24, 54], [24, 49], [19, 49], [15, 51], [15, 54]]] } },
                { "type": "Feature", "id": "FRA", "properties": { "name": "France" }, "geometry": { "type": "Polygon", "coordinates": [[[2, 51], [8, 49], [7, 43], [0, 43], [-2, 48], [2, 51]]] } },
                { "type": "Feature", "id": "GBR", "properties": { "name": "United Kingdom" }, "geometry": { "type": "Polygon", "coordinates": [[[-5, 58], [0, 61], [2, 51], [-4, 50], [-5, 58]]] } },
                { "type": "Feature", "id": "ITA", "properties": { "name": "Italy" }, "geometry": { "type": "Polygon", "coordinates": [[[8, 46], [13, 46], [18, 40], [14, 37], [10, 37], [7, 44], [8, 46]]] } },
                { "type": "Feature", "id": "SUN", "properties": { "name": "Soviet Union" }, "geometry": { "type": "Polygon", "coordinates": [[[30, 70], [45, 65], [60, 60], [50, 40], [30, 42], [24, 50], [30, 70]]] } },
                { "type": "Feature", "id": "JPN", "properties": { "name": "Japan" }, "geometry": { "type": "Polygon", "coordinates": [[[130, 45], [145, 45], [145, 30], [130, 30], [130, 45]]] } },
                { "type": "Feature", "id": "USA", "properties": { "name": "United States" }, "geometry": { "type": "Polygon", "coordinates": [[[-125, 49], [-66, 49], [-66, 25], [-125, 25], [-125, 49]]] } },
                { "type": "Feature", "id": "CHN", "properties": { "name": "China" }, "geometry": { "type": "Polygon", "coordinates": [[[75, 50], [100, 50], [130, 42], [130, 20], [98, 20], [75, 30], [75, 50]]] } },
                { "type": "Feature", "id": "BEL", "properties": { "name": "Belgium" }, "geometry": { "type": "Polygon", "coordinates": [[[2.5, 51.5], [6, 51], [6, 49.5], [3, 49.5], [2.5, 51.5]]] } },
                { "type": "Feature", "id": "NLD", "properties": { "name": "Netherlands" }, "geometry": { "type": "Polygon", "coordinates": [[[3, 53.5], [7, 53.5], [7, 51], [3, 51], [3, 53.5]]] } },
                { "type": "Feature", "id": "NOR", "properties": { "name": "Norway" }, "geometry": { "type": "Polygon", "coordinates": [[[4, 62], [12, 64], [30, 71], [10, 59], [4, 62]]] } },
                { "type": "Feature", "id": "SWE", "properties": { "name": "Sweden" }, "geometry": { "type": "Polygon", "coordinates": [[[12, 69], [24, 69], [24, 55], [12, 55], [12, 69]]] } },
                { "type": "Feature", "id": "DNK", "properties": { "name": "Denmark" }, "geometry": { "type": "Polygon", "coordinates": [[[8, 57], [13, 57], [13, 54], [8, 54], [8, 57]]] } },
                { "type": "Feature", "id": "FIN", "properties": { "name": "Finland" }, "geometry": { "type": "Polygon", "coordinates": [[[20, 70], [32, 70], [32, 60], [20, 60], [20, 70]]] } },
                { "type": "Feature", "id": "AUT", "properties": { "name": "Austria" }, "geometry": { "type": "Polygon", "coordinates": [[[9, 48], [17, 48], [17, 46], [9, 46], [9, 48]]] } },
                { "type": "Feature", "id": "CZE", "properties": { "name": "Czechoslovakia" }, "geometry": { "type": "Polygon", "coordinates": [[[12, 51], [19, 51], [19, 48], [12, 48], [12, 51]]] } },
                { "type": "Feature", "id": "YUG", "properties": { "name": "Yugoslavia" }, "geometry": { "type": "Polygon", "coordinates": [[[13, 46], [23, 46], [23, 40], [13, 40], [13, 46]]] } },
                { "type": "Feature", "id": "ROM", "properties": { "name": "Romania" }, "geometry": { "type": "Polygon", "coordinates": [[[20, 48], [30, 48], [30, 43], [20, 43], [20, 48]]] } },
                { "type": "Feature", "id": "BUL", "properties": { "name": "Bulgaria" }, "geometry": { "type": "Polygon", "coordinates": [[[22, 44], [28, 44], [28, 41], [22, 41], [22, 44]]] } },
                { "type": "Feature", "id": "HUN", "properties": { "name": "Hungary" }, "geometry": { "type": "Polygon", "coordinates": [[[16, 48], [23, 48], [23, 45], [16, 45], [16, 48]]] } },
                { "type": "Feature", "id": "GRC", "properties": { "name": "Greece" }, "geometry": { "type": "Polygon", "coordinates": [[[19, 42], [25, 42], [25, 35], [19, 35], [19, 42]]] } },
                { "type": "Feature", "id": "ESP", "properties": { "name": "Spain" }, "geometry": { "type": "Polygon", "coordinates": [[[-9, 43], [3, 43], [3, 36], [-9, 36], [-9, 43]]] } },
                { "type": "Feature", "id": "PRT", "properties": { "name": "Portugal" }, "geometry": { "type": "Polygon", "coordinates": [[[-9, 42], [-6, 42], [-6, 37], [-9, 37], [-9, 42]]] } },
                { "type": "Feature", "id": "PHI", "properties": { "name": "Philippines" }, "geometry": { "type": "Polygon", "coordinates": [[[120, 20], [126, 20], [126, 5], [120, 5], [120, 20]]] } },
                { "type": "Feature", "id": "EGY", "properties": { "name": "Egypt" }, "geometry": { "type": "Polygon", "coordinates": [[[25, 32], [35, 32], [35, 22], [25, 22], [25, 32]]] } },
                { "type": "Feature", "id": "LBY", "properties": { "name": "Libya" }, "geometry": { "type": "Polygon", "coordinates": [[[10, 33], [25, 33], [25, 20], [10, 20], [10, 33]]] } },
                { "type": "Feature", "id": "MAR", "properties": { "name": "Morocco" }, "geometry": { "type": "Polygon", "coordinates": [[[-10, 35], [10, 35], [10, 28], [-10, 28], [-10, 35]]] } },
                { "type": "Feature", "id": "DZA", "properties": { "name": "Algeria" }, "geometry": { "type": "Polygon", "coordinates": [[[-5, 37], [10, 37], [10, 30], [-5, 30], [-5, 37]]] } },
            ]
        };

        // WW2 territorial control data (simplified for this demo)
        const territorialChanges = [
            {
                date: new Date(1939, 8, 1), // September 1, 1939
                territories: {
                    "DEU": "germany",
                    "POL": "neutral",
                    "FRA": "france",
                    "GBR": "uk",
                    "ITA": "italy",
                    "SUN": "ussr",
                    "JPN": "japan",
                    "USA": "usa",
                    "CHN": "neutral",
                    "BEL": "neutral",
                    "NLD": "neutral",
                    "NOR": "neutral",
                    "SWE": "neutral",
                    "DNK": "neutral",
                    "FIN": "neutral",
                    "AUT": "germany", // Annexed in 1938
                    "CZE": "germany", // Occupied March 1939
                    "YUG": "neutral",
                    "ROM": "neutral",
                    "BUL": "neutral",
                    "HUN": "neutral",
                    "GRC": "neutral",
                    "ESP": "neutral",
                    "PRT": "neutral",
                    "PHI": "usa", // US territory
                    "EGY": "uk", // British influence
                    "LBY": "italy", // Italian colony
                    "MAR": "france", // French colony
                    "DZA": "france", // French colony
                },
                events: "Germany invades Poland on September 1, 1939, marking the beginning of World War II in Europe."
            },
            {
                date: new Date(1939, 8, 17), // September 17, 1939
                territories: {
                    "POL": "split", // Split between Germany and USSR
                },
                events: "Soviet Union invades Poland from the east. Poland is divided between Nazi Germany and the Soviet Union."
            },
            {
                date: new Date(1939, 10, 30), // November 30, 1939
                territories: {
                    "FIN": "warWith", // War with USSR
                },
                events: "Soviet Union invades Finland, starting the Winter War."
            },
            {
                date: new Date(1940, 3, 13), // April 9, 1940
                territories: {
                    "DNK": "germany", // German occupation
                    "NOR": "germany", // German occupation
                },
                events: "Germany invades Denmark and Norway. Denmark surrenders in less than a day, while Norway fights until June."
            },
            {
                date: new Date(1940, 4, 10), // May 10, 1940
                territories: {
                    "BEL": "germany", // German occupation
                    "NLD": "germany", // German occupation
                    "LUX": "germany", // German occupation
                },
                events: "Germany invades the Netherlands, Belgium, and Luxembourg. The Netherlands surrenders on May 14, Belgium on May 28."
            },
            {
                date: new Date(1940, 5, 22), // June 22, 1940
                territories: {
                    "FRA": "split", // Part German-occupied, part Vichy
                },
                events: "France signs an armistice with Germany. Northern France is occupied by Germany, while southern France remains under the control of the Vichy government, a German puppet state."
            },
            {
                date: new Date(1940, 8, 27), // September 27, 1940
                territories: {
                    "JPN": "japan", // emphasize Japan's expansion
                },
                events: "Japan signs the Tripartite Pact with Germany and Italy, formally creating the Axis Powers."
            },
            {
                date: new Date(1941, 3, 6), // April 6, 1941
                territories: {
                    "YUG": "axis", // Axis occupation
                    "GRC": "axis", // Axis occupation
                },
                events: "Germany, Italy, and Hungary invade Yugoslavia and Greece. Both countries are defeated and occupied by Axis powers."
            },
            {
                date: new Date(1941, 5, 22), // June 22, 1941
                territories: {
                    "SUN": "warWith", // War with Germany
                },
                events: "Germany launches Operation Barbarossa, invading the Soviet Union with the largest invasion force in history."
            },
            {
                date: new Date(1941, 11, 7), // December 7, 1941
                territories: {
                    "USA": "warWith", // War with Japan
                    "PHI": "warWith", // Soon to be occupied by Japan
                },
                events: "Japan attacks Pearl Harbor, bringing the United States into the war. Japanese forces also attack the Philippines, Hong Kong, and Malaya."
            },
            {
                date: new Date(1941, 11, 11), // December 11, 1941
                territories: {
                    "USA": "allies", // Now formally at war with all Axis
                },
                events: "Germany and Italy declare war on the United States."
            },
            {
                date: new Date(1942, 5, 4), // June 4, 1942
                territories: {
                    "PHI": "japan", // Japanese occupation
                    "CHN": "split", // Partially occupied by Japan
                },
                events: "The Battle of Midway marks a turning point in the Pacific War, with Japan suffering a decisive naval defeat. However, Japan still controls vast territories in Asia including parts of China, the Philippines, and Southeast Asia."
            },
            {
                date: new Date(1942, 10, 23), // November 23, 1942
                territories: {
                    "SUN": "defendingEast", // Soviets holding at Stalingrad
                },
                events: "Soviet forces launch Operation Uranus, encircling German forces at Stalingrad. This marks the beginning of a major turning point on the Eastern Front."
            },
            {
                date: new Date(1943, 1, 31), // February 2, 1943
                territories: {
                    "SUN": "pushingWest", // Soviets beginning counter-offensive
                },
                events: "German forces surrender at Stalingrad, marking a decisive defeat for the Axis on the Eastern Front. The Soviet Union begins its long push westward."
            },
            {
                date: new Date(1943, 6, 10), // July 10, 1943
                territories: {
                    "ITA": "invaded", // Allied invasion of Sicily
                },
                events: "Allied forces land in Sicily, beginning the Italian Campaign."
            },
            {
                date: new Date(1943, 8, 8), // September 8, 1943
                territories: {
                    "ITA": "split", // Italy surrenders but Germany occupies
                },
                events: "Italy surrenders to the Allies. Germany quickly occupies northern Italy and continues fighting."
            },
            {
                date: new Date(1944, 5, 6), // June 6, 1944
                territories: {
                    "FRA": "invaded", // D-Day landings
                },
                events: "D-Day: Allied forces land in Normandy, beginning the liberation of Western Europe."
            },
            {
                date: new Date(1944, 7, 20), // August 20, 1944
                territories: {
                    "FRA": "allies", // France being liberated
                    "BEL": "allies", // Belgium being liberated
                },
                events: "Paris is liberated by Allied forces. Most of France is freed from German occupation."
            },
            {
                date: new Date(1944, 11, 16), // December 16, 1944
                territories: {
                    "BEL": "battleground", // Battle of the Bulge
                },
                events: "Germany launches its last major offensive in the west, the Battle of the Bulge, through the Ardennes Forest in Belgium and Luxembourg."
            },
            {
                date: new Date(1945, 1, 27), // February 27, 1945
                territories: {
                    "DEU": "invaded", // Germany being invaded from both sides
                    "POL": "ussr", // Now under Soviet control
                    "ROM": "ussr", // Now under Soviet control
                    "BUL": "ussr", // Now under Soviet control
                    "HUN": "ussr", // Now under Soviet control
                    "YUG": "ussr", // Now under Soviet influence
                },
                events: "Soviet forces continue their advance into Germany, while Allied forces cross the Rhine River into western Germany."
            },
            {
                date: new Date(1945, 4, 30), // May 8, 1945
                territories: {
                    "DEU": "split", // Split between Allies and Soviets
                    "AUT": "split", // Split between Allies and Soviets
                    "ITA": "allies", // Fully under Allied control
                    "FRA": "allies", // Fully liberated
                    "BEL": "allies", // Fully liberated
                    "NLD": "allies", // Fully liberated
                    "NOR": "allies", // Fully liberated
                    "DNK": "allies", // Fully liberated
                    "CZE": "ussr", // Under Soviet control
                    "POL": "ussr", // Under Soviet control
                },
                events: "Victory in Europe Day (VE Day): Germany surrenders unconditionally, ending World War II in Europe."
            },
            {
                date: new Date(1945, 7, 14), // August 14, 1945
                territories: {
                    "JPN": "defeated", // Japan defeated
                    "CHN": "split", // Civil war brewing in China
                    "PHI": "usa", // Returned to US control
                },
                events: "Japan announces its surrender after atomic bombings of Hiroshima and Nagasaki and the Soviet invasion of Manchuria, ending World War II."
            }
        ];

        // Country labels
        const countryLabels = {
            "DEU": { x: 10, y: 51, name: "Germany" },
            "POL": { x: 19, y: 52, name: "Poland" },
            "FRA": { x: 3, y: 47, name: "France" },
            "GBR": { x: -2, y: 55, name: "UK" },
            "ITA": { x: 12, y: 42, name: "Italy" },
            "SUN": { x: 40, y: 55, name: "USSR" },
            "JPN": { x: 135, y: 38, name: "Japan" },
            "USA": { x: -100, y: 40, name: "USA" },
            "CHN": { x: 100, y: 35, name: "China" },
            "ESP": { x: -5, y: 40, name: "Spain" },
            "FIN": { x: 25, y: 65, name: "Finland" },
        };

        // Color mapping for different controls
        const colorMap = {
            "neutral": "#808080",
            "germany": "#444444",
            "axis": "#940000",
            "italy": "#008C45",
            "japan": "#BC002D",
            "allies": "#004b87",
            "uk": "#00247D",
            "france": "#002654",
            "usa": "#3C3B6E",
            "ussr": "#CC0000",
            "split": "#8B4513",
            "warWith": "#FF0000",
            "invaded": "#FFD700",
            "battleground": "#8B008B",
            "defendingEast": "#4682B4",
            "pushingWest": "#1E90FF",
            "defeated": "#000000"
        };

        let isPlaying = false;
        let animationFrame;
        const startDate = new Date(1939, 8, 1);
        const endDate = new Date(1945, 7, 14);
        const totalDuration = endDate - startDate;
        let currentDate = new Date(startDate);

        // Initialize the map
        function initMap() {
            const mapGroup = document.getElementById('map-group');
            const labelsGroup = document.getElementById('labels');
            
            // Create country shapes
            mapData.features.forEach(feature => {
                const country = document.createElementNS('http://www.w3.org/2000/svg', 'path');
                const id = feature.id;
                
                // Create a path string from the coordinates
                let pathData = '';
                feature.geometry.coordinates.forEach(ring => {
                    ring.forEach((coord, i) => {
                        const [x, y] = coord;
                        pathData += (i === 0 ? 'M' : 'L') + (x * 3 + 500) + ',' + (300 - y * 3);
                    });
                    pathData += 'Z';
                });
                
                country.setAttribute('d', pathData);
                country.setAttribute('id', 'country-' + id);
                country.setAttribute('class', 'country');
                country.setAttribute('data-id', id);
                
                // Add tooltip
                country.setAttribute('title', feature.properties.name);
                
                mapGroup.appendChild(country);
                
                // Add label if it exists in our labels collection
                if (countryLabels[id]) {
                    const label = document.createElementNS('http://www.w3.org/2000/svg', 'text');
                    const { x, y, name } = countryLabels[id];
                    
                    label.setAttribute('x', x * 3 + 500);
                    label.setAttribute('y', 300 - y * 3);
                    label.setAttribute('class', 'country-label text-xs font-medium pointer-events-none');
                    label.textContent = name;
                    
                    labelsGroup.appendChild(label);
                }
            });
            
            // Apply initial territorial control
            updateTerritories(territorialChanges[0]);
        }

        // Update territories based on a specific timepoint
        function updateTerritories(timepoint) {
            const territories = timepoint.territories;
            
            // Update each territory's control
            for (const [id, control] of Object.entries(territories)) {
                const country = document.getElementById('country-' + id);
                if (country) {
                    country.style.fill = colorMap[control] || '#808080';
                }
            }
            
            // Update event information
            document.getElementById('event-info').innerHTML = `<p>${timepoint.events}</p>`;
            
            // Update date display
            const options = { year: 'numeric', month: 'long' };
            document.getElementById('date-display').textContent = timepoint.date.toLocaleDateString(undefined, options);
        }

        // Find the appropriate timepoint for a given date
        function findTimepoint(date) {
            // Start from the most recent and work backwards
            for (let i = territorialChanges.length - 1; i >= 0; i--) {
                if (date >= territorialChanges[i].date) {
                    return territorialChanges[i];
                }
            }
            return territorialChanges[0];
        }

        // Update the timeline position based on current date
        function updateTimeline() {
            const progress = (currentDate - startDate) / totalDuration * 100;
            document.getElementById('timeline-progress').style.width = progress + '%';
            document.getElementById('timeline-marker').style.left = progress + '%';
        }

        // Animation loop
        function animate() {
            if (!isPlaying) return;
            
            // Move forward 1 month
            currentDate = new Date(currentDate.setMonth(currentDate.getMonth() + 1));
            
            // Check if we've reached the end
            if (currentDate > endDate) {
                currentDate = new Date(endDate);
                togglePlay(false);
            }
            
            // Update map and timeline
            updateTimeline();
            updateTerritories(findTimepoint(currentDate));
            
            // Continue animation
            animationFrame = requestAnimationFrame(animate);
        }

        // Toggle play/pause
        function togglePlay(play) {
            const playPauseBtn = document.getElementById('play-pause');
            const icon = playPauseBtn.querySelector('svg');
            const text = playPauseBtn.querySelector('span');
            
            isPlaying = play === undefined ? !isPlaying : play;
            
            if (isPlaying) {
                // Play icon to pause icon
                icon.innerHTML = `<path fill-rule="evenodd" d="M18 10a8 8 0 11-16 0 8 8 0 0116 0zM7 8a1 1 0 012 0v4a1 1 0 11-2 0V8zm5-1a1 1 0 00-1 1v4a1 1 0 102 0V8a1 1 0 00-1-1z" clip-rule="evenodd" />`;
                text.textContent = 'Pause';
                animate();
            } else {
                // Pause icon to play icon
                icon.innerHTML = `<path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd" />`;
                text.textContent = 'Play';
                cancelAnimationFrame(animationFrame);
            }
        }

        // Timeline slider interaction
        function initTimelineInteraction() {
            const timelineTrack = document.querySelector('.timeline-track');
            const timelineMarker = document.getElementById('timeline-marker');
            
            function setPositionFromEvent(e) {
                // Calculate position
                const rect = timelineTrack.getBoundingClientRect();
                let x = e.clientX - rect.left;
                if (x < 0) x = 0;
                if (x > rect.width) x = rect.width;
                
                // Calculate percentage and update date
                const percentage = x / rect.width;
                currentDate = new Date(startDate.getTime() + totalDuration * percentage);
                
                // Update UI
                updateTimeline();
                updateTerritories(findTimepoint(currentDate));
            }
            
            // Mouse events
            timelineTrack.addEventListener('mousedown', (e) => {
                setPositionFromEvent(e);
                
                // Add drag handlers
                document.addEventListener('mousemove', setPositionFromEvent);
                document.addEventListener('mouseup', () => {
                    document.removeEventListener('mousemove', setPositionFromEvent);
                }, { once: true });
            });
            
            // Touch events for mobile
            timelineTrack.addEventListener('touchstart', (e) => {
                e.preventDefault();
                setPositionFromEvent(e.touches[0]);
                
                // Add drag handlers
                document.addEventListener('touchmove', (e) => {
                    e.preventDefault();
                    setPositionFromEvent(e.touches[0]);
                });
                
                document.addEventListener('touchend', () => {
                    document.removeEventListener('touchmove', setPositionFromEvent);
                }, { once: true });
            });
            
            // Click directly on the track
            timelineTrack.addEventListener('click', setPositionFromEvent);
        }

        // Reset button
        document.getElementById('reset').addEventListener('click', () => {
            togglePlay(false);
            currentDate = new Date(startDate);
            updateTimeline();
            updateTerritories(findTimepoint(currentDate));
        });

        // Play/pause button
        document.getElementById('play-pause').addEventListener('click', () => togglePlay());

        // Initialize map and controls
        initMap();
        initTimelineInteraction();
    </script>
</body>
</html>
