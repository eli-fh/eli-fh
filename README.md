<!DOCTYPE html>
<html lang="he">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>עמוד בחירת מושבים</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            padding: 50px;
        }
        #main {
            padding: 20px;
            border: 2px solid #ddd;
            background: #fff;
            display: inline-block;
            border-radius: 8px;
        }
        h1 {
            color: #333;
        }
        .seat {
            width: 30px;
            height: 30px;
            background: #28a745;
            border: 1px solid #ddd;
            margin: 5px;
            display: inline-block;
            cursor: pointer;
            transition: background 0.3s;
        }
        .seat.taken {
            background: #ff4d4d;
        }
    </style>
</head>
<body>
    <div id="main">
        <h1>בחר את המושב שלך</h1>
        <div id="seats">
            <!-- יצירת 30 מושבים לדוגמה -->
            <script>
                for(let i = 1; i <= 30; i++) {
                    document.write('<div class="seat" id="seat-' + i + '" onclick="toggleSeat(' + i + ')"></div>');
                }
            </script>
        </div>
    </div>

    <script>
        // פונקציה להחלפת מצב מושב (פנוי / תפוס)
        function toggleSeat(seatNumber) {
            var seat = document.getElementById('seat-' + seatNumber);
            seat.classList.toggle('taken');
        }
    </script>
</body>
</html>
