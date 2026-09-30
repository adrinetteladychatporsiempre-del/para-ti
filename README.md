# para-ti
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Página de regalo especial para Elmer Orlando">
    <title>Solo para ti</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #ff416c, #ff4b2b);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            color: #fff;
            text-align: center;
            padding: 20px;
        }

        .container {
            position: relative;
            z-index: 10;
            max-width: 500px;
            width: 100%;
        }

        h1 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            text-shadow: 0 3px 6px rgba(0,0,0,0.3);
            animation: fadeInDown 1s ease;
        }

        .shining-name {
            display: inline-block;
            font-size: 2.5rem;
            font-weight: 800;
            color: #fff5cc;
            text-shadow: 0 0 10px #ffea75, 0 0 20px #ffcc00, 0 0 30px #ff9900, 0 0 40px #ff6600;
            animation: shine 2s infinite alternate ease-in-out;
            margin-bottom: 10px;
            letter-spacing: 1px;
        }

        @keyframes shine {
            0% {
                color: #fff5cc;
                text-shadow: 0 0 10px #ffea75, 0 0 20px #ffcc00, 0 0 30px #ff9900;
                transform: scale(1);
            }
            100% {
                color: #ffffff;
                text-shadow: 0 0 20px #ffffff, 0 0 30px #ffea75, 0 0 40px #ffcc00, 0 0 50px #ff9900;
                transform: scale(1.03);
            }
        }

        .gift-box {
            position: relative;
            width: 180px;
            height: 180px;
            background: #ffcc00;
            margin: 20px auto;
            border-radius: 15px;
            cursor: pointer;
            box-shadow: 0 10px 25px rgba(0,0,0,0.3);
            transition: transform 0.3s ease;
            animation: bounce 2s infinite;
        }

        .gift-box:hover {
            transform: scale(1.05);
        }

        .gift-lid {
            position: absolute;
            top: -20px;
            left: -10px;
            width: 200px;
            height: 40px;
            background: #ff3366;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.5s ease, top 0.5s ease;
        }

        .ribbon-vertical {
            position: absolute;
            top: 0;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 30px;
            background: #ff3366;
        }

        .gift-lid .ribbon-vertical {
            top: -20px;
            height: 40px;
        }

        .ribbon-horizontal {
            position: absolute;
            top: 50%;
            left: 0;
            right: 0;
            transform: translateY(-50%);
            height: 30px;
            background: #ff3366;
        }

        .message-card {
            display: none;
            background: white;
            color: #333;
            padding: 25px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.3);
            animation: zoomIn 0.8s ease forwards;
            margin-top: 20px;
        }

        .message-card h2 {
            color: #ff3366;
            margin-bottom: 10px;
            font-size: 1.8