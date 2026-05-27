<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>One Piece</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            padding: 0;
            min-height: 100vh;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background-image: url('https://www.dropbox.com/scl/fi/sy09wy53els7tlwzrje72/14c5c657-f817-4537-841c-1ead968e39ab.jpeg?rlkey=20248pmcwcvmop4z53r4ny80c&raw=1');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #ffffff;
            overflow-x: hidden;
        }

        body::before {
            content: "";
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.45);
            z-index: -1;
        }

        .glass-container {
            width: 90%;
            max-width: 1200px;
            margin: 40px auto;
            padding: 40px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5rem;
            margin: 0 0 10px 0;
            font-weight: 600;
            letter-spacing: 1px;
            text-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.1rem;
            opacity: 0.8;
            margin: 0;
        }

        .media-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .media-card {
            background: rgba(0, 0, 0, 0.2);
            padding: 20px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
            animation: fadeIn 1s ease;
        }

        .media-card:hover {
            transform: translateY(-5px);
        }

        .media-card h2 {
            font-size: 1.2rem;
            margin-top: 0;
            margin-bottom: 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
            padding-bottom: 10px;
        }

        .media-wrapper {
            position: relative;
            width: 100%;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .video-wrapper {
            padding-bottom: 56.25%;
            height: 0;
        }

        .video-wrapper video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            background-color: #000;
        }

        .audio-wrapper {
            padding: 20px;
            background: rgba(255, 255, 255, 0.05);
            display: flex;
            justify-content: center;
        }

        audio {
            width: 100%;
            outline: none;
        }

        .map-wrapper {
            padding-bottom: 75%;
            height: 0;
        }

        .map-wrapper iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: 0;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 768px) {
            .glass-container {
                padding: 20px;
            }

            header h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <div class="glass-container">
        <header>
            <h1>One Piece</h1>
            <p>Video and Audio/ Embedded Map</p>
        </header>

        <div class="media-grid">
            
            <div class="media-card">
                <h2>One Piece Video</h2>
                <div class="media-wrapper video-wrapper">
                    <video controls>
                        <source src="https://www.dropbox.com/scl/fi/q1sa38t757hrfcf2ed3dd/e9a7ef0e0ea10cdd3a5d6c5defd5ab26.mp4?rlkey=npshbtnwb7qhpyn14va6qrwjy&raw=1" type="video/mp4">
                        Your browser does not support the video tag.
                    </video>
                </div>
            </div>

            <div class="media-card">
                <h2>Binks Sake Audio</h2>
                <div class="media-wrapper audio-wrapper">
                    <audio controls>
                        <source src="https://www.dropbox.com/scl/fi/9zhuqjdlsufre0k36u583/one-piece-mania_bink-s-sake-strawhat-crew-version.mp3?rlkey=e8yv6ucykfhpe09tp1ialsl5h&raw=1" type="audio/mpeg">
                    </audio>
                </div>
            </div>

            <div class="media-card">
                <h2>Rodriguez Map</h2>
                <div class="media-wrapper map-wrapper">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d123473.11195610815!2d121.1111603590518!3d14.735165600000003!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3397bb6d7a4bd53d%3A0xc3f6e166f2bc8a67!2sRodriguez%2C%20Rizal%2C%20Philippines!5e0!3m2!1sen!2sus!4v1680000000000!5m2!1sen!2sus" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>

        </div>
    </div>

</body>
</html>

