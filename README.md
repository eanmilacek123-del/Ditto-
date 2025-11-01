# Ditto-dark-dance
Ditto dance
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ditto's Hour of Death</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #0f0f0f, #1a0033);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: 'Courier New', monospace;
            color: #ff69b4; /* Pink text for Ditto vibes */
            overflow: hidden;
        }
        #container {
            text-align: center;
        }
        button {
            background: #ff1493;
            color: #000;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            border-radius: 5px;
            transition: transform 0.2s;
        }
        button:hover {
            transform: scale(1.05);
        }
        #video-container {
            display: none;
            width: 100vw;
            height: 100vh;
            position: fixed;
            top: 0;
            left: 0;
            z-index: 10;
        }
        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        h1 {
            font-size: 2em;
            text-shadow: 0 0 10px #ff69b4;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>
    <div id="container">
        <h1>matias.me/hour-of-death</h1>
        <p style="font-size: 14px; margin-bottom: 20px;">(A darker twist on the classic... Trust the slime?)</p>
        <button onclick="startTheChaos()">Click if you dare...</button>
    </div>
    <div id="video-container">
        <video id="danceVideo" autoplay loop muted>
            <source src="https://archive.org/download/DittoDance/DittoDance.mp4" type="video/mp4">
            <!-- Fallback: If you want to host your own Ditto animation, replace the src with your file URL -->
            Your browser doesn't support video—time to upgrade, sinner.
        </video>
        <audio id="track" loop>
            <source src="https://audio-0-9-prod-vi-songs.akamaized.net/assets/songs/5g3PPNIHL5yMci2pio9ZoI/Now_and_at_the_Hour_of_Our_Death_feat_BONES_320.mp3" type="audio/mpeg">
            <!-- Note: This is a placeholder for the track. For legal sharing, embed from Spotify/YouTube or use a free soundboard clip. Replace with your hosted MP3. -->
            Audio not supported—pray for us sinners.
        </audio>
    </div>

    <script>
        function startTheChaos() {
            document.getElementById('container').style.display = 'none';
            const videoContainer = document.getElementById('video-container');
            videoContainer.style.display = 'block';
            
            const video = document.getElementById('danceVideo');
            const audio = document.getElementById('track');
            
            video.play();
            audio.play();
            
            // Sync animation energy: Add some CSS shake to the video for "energetic" feel
            videoContainer.style.animation = 'shake 0.5s infinite';
            
            // Add shake keyframes dynamically
            const style = document.createElement('style');
            style.textContent = `
                @keyframes shake {
                    0%, 100% { transform: translateX(0); }
                    25% { transform: translateX(-5px); }
                    75% { transform: translateX(5px); }
                }
            `;
            document.head.appendChild(style);
        }
        
        // Auto-start on load for max prank (uncomment if desired)
        // window.onload = startTheChaos;
    </script>
</body>
</html>
