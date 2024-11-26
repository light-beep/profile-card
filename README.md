<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Profile & Image Overlay</title>
    <style>
        /* Your existing CSS styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-image: url('https://i.ibb.co/nBjdCy9/images-78.jpg');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            color: white;
        }

        h2, h1, h3 {
            text-align: center;
            margin-top: 20px;
        }

        h3 {
            color: #FFD700;
        }

        .row {
            display: flex;
            justify-content: center;
            flex-wrap: wrap; /* Allows content to wrap on smaller screens */
            gap: 15px; /* Adds space between images */
            margin-top: 20px;
        }

        .container {
            position: relative;
            width: 20%; /* Adjusted for responsiveness */
            height: auto; /* Maintain aspect ratio */
            max-width: 150px; /* Limit container size on larger screens */
            margin: 10px;
            border: 5px solid #27bfe6; /* Blue border for better contrast */
            border-radius: 5px; /* Rounded corners */
            overflow: hidden; /* Ensures overlay fits inside borders */
        }

        .image {
            display: block;
            width: 100%;
            height: 100%;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5); /* Transparent black overlay */
            display: flex;
            justify-content: center; /* Centers content horizontally */
            align-items: center; /* Centers content vertically */
            flex-direction: column;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .overlay img {
            max-width: 100%;
            max-height: 100%;
            filter: blur(5px); /* Blurs the overlay image */
            transition: filter 0.3s ease;
        }

        .overlay p {
            margin-top: 10px;
            color: white;
            font-size: 14px;
            font-weight: bold;
            text-align: center; /* Centers the text horizontally */
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .container:hover .overlay {
            opacity: 1;
        }

        .container:hover .overlay img {
            filter: blur(8px); /* Intensifies blur on hover */
        }

        .container:hover .overlay p {
            opacity: 1; /* Makes the text visible */
        }

        a {
            text-decoration: none;
        }

        button {
            background-color: white;
            color: black;
            border: none;
            padding: 10px 20px;
            cursor: pointer;
            display: block;
            margin: 20px auto;
            font-size: 16px;
            width: auto; /* Allow button to shrink for smaller screens */
        }

        button:hover {
            background-color: #FFD700;
            color: black;
        }

        @media (max-width: 768px) {
            .row {
                flex-direction: column; /* Stack content vertically on small screens */
                align-items: center;
            }

            .container {
                width: 80%; /* Expand containers on smaller screens */
                max-width: none; /* Remove the size limit */
            }

            h1, h2, h3, p {
                font-size: smaller; /* Adjust text sizes for readability */
            }

            button {
                width: 80%; /* Resize button */
            }
        }
    </style>
</head>
<body>
    <center>
        <h1>Welcome to my profile card</h1>
        <h3>I am <span>JOYETTE SILAO</span></h3>
        <img src="https://i.ibb.co/Yk7vwnD/inbound217031560924243871.jpg" width="50%" height="auto" alt="Profile Image" />
        <br />
        <h1>About Myself</h1>
        <hr />
        <p>Hello! I’m Joyette Silao, an 18-year-old Computer Science student from ISAT University, hailing from Calinog, Iloilo. Currently, I serve as the Vice Mayor of our section, BCSC 1-B. I have a passion for coding, particularly in Java and JavaScript, and enjoy honing my programming skills. Besides academics, I’m also a skilled dancer and a gamer, often playing games like Call of Duty Mobile (CODM) and Mobile Legends.</p>
        <br /><br />

        <h2>Options</h2>

        <div class="row">
            <!-- Options for social links -->
            <a href="https://www.tiktok.com/@csts_light?_t=8ri03MlPCyo&_r=1">
                <div class="container">
                    <img src="https://i.ibb.co/W36g1Zw/download.png" alt="TikTok" class="image">
                    <div class="overlay">
                        <img src="https://i.ibb.co/WpMzyLZ/images-63.jpg" alt="Overlay TikTok">
                        <p>TikTok</p>
                    </div>
                </div>
            </a>

            <a href="https://www.instagram.com/joyettesilao/profilecard/?igsh=MTdxeXA3aXF1YzlhYQ==">
                <div class="container">
                    <img src="https://i.ibb.co/7S4nX8Q/images-79.jpg" alt="Instagram" class="image">
                    <div class="overlay">
                        <img src="https://i.ibb.co/WpMzyLZ/images-63.jpg" alt="Overlay Instagram">
                        <p>Instagram</p>
                    </div>
                </div>
            </a>

            <a href="https://www.facebook.com/joyette.silao.5">
                <div class="container">
                    <img src="https://i.ibb.co/64SffLH/fb-icon-325x325.png" alt="Facebook" class="image">
                    <div class="overlay">
                        <img src="https://i.ibb.co/WpMzyLZ/images-63.jpg" alt="Overlay Facebook">
                        <p>Facebook</p>
                    </div>
                </div>
            </a>
        </div>

        <button onclick="exitPage()">Exit</button>
    </center>

    <script>
        function exitPage() {
            alert('Thank you for visiting!'); // Optional user feedback
            window.location.href = "https://your-url-here.com"; // Redirect to a new page
        }
    </script>
</body>
</html>
