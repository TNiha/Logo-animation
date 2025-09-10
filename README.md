<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Logo Intro</title>
    <!-- Tailwind CSS for modern styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Apply a subtle background gradient and the 'Inter' font to the body */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #1a202c; /* A dark, professional background color */
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        /*
         * Keyframe animations for the intro sequence.
         * The animations are designed to create a smooth, clean reveal.
         */
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes scaleUp {
            from {
                transform: scale(0.8);
            }
            to {
                transform: scale(1);
            }
        }

        @keyframes slideIn {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /*
         * A custom class to apply the animations.
         * We'll use a small delay to create a sequential reveal effect.
         */
        .logo-container {
            animation: fadeIn 1.5s ease-out forwards;
        }

        .logo-icon {
            animation: scaleUp 1.0s ease-out 1.2s forwards;
            opacity: 0;
        }

        .logo-text {
            animation: slideIn 1.0s ease-out 1.5s forwards;
            opacity: 0;
        }

        /*
         * You can replace the text-based logo with an SVG or image.
         * For example:
         * .logo-icon {
         * width: 100px;
         * height: 100px;
         * background-image: url('your-logo.svg');
         * background-size: contain;
         * background-repeat: no-repeat;
         * }
         */
    </style>
</head>
<body class="flex flex-col items-center justify-center bg-gray-900">

    <!-- Main container for the logo, centered on the page -->
    <div class="logo-container text-center text-white">

        <!-- Logo icon placeholder (could be an SVG or image) -->
        <div class="logo-icon w-24 h-24 sm:w-32 sm:h-32 mx-auto rounded-full bg-blue-600 flex items-center justify-center mb-4 transform scale-0 opacity-0 shadow-lg">
            <!-- A simple SVG circle for demonstration -->
            <svg class="w-12 h-12 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2z"/>
            </svg>
        </div>

        <!-- Logo text placeholder -->
        <h1 class="logo-text text-3xl sm:text-5xl font-extrabold tracking-tight opacity-0">
            Your Logo Here
        </h1>
    </div>

</body>
</html>
