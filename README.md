<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Professional Dashboard</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">
    
    <style>
        /* CSS Styling for a professional, dark-mode UI */

        /* Custom properties for easy color changes */
        :root {
            --bg-color: #1a1a2e; /* Dark background */
            --text-color: #ffffff; /* White text */
            --card-bg: #2c2c45; /* Slightly lighter card background */
            --accent-color: #4a4e69; /* Subtle accent/border color */
            --hover-color: #6a00ff; /* Bright purple hover color */
            --font-stack: 'Arial', sans-serif;
        }

        /* Global Reset and Body Styling */
        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: var(--font-stack);
            margin: 0;
            padding: 20px;
            line-height: 1.6;
            min-height: 100vh;
            box-sizing: border-box;
        }

        /* Header Styling */
        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5em;
            margin-bottom: 5px;
            font-weight: 700;
        }

        header p {
            font-size: 1.1em;
            color: #b0b0b0; /* Light gray for subtext */
        }

        /* Search Bar Styling */
        .search-container {
            max-width: 600px;
            margin: 0 auto 50px auto;
        }

        #search-form {
            display: flex;
            border-radius: 30px;
            overflow: hidden;
            background-color: var(--card-bg);
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5); /* Deep shadow */
        }

        #search-input {
            flex-grow: 1;
            border: none;
            padding: 15px 25px;
            font-size: 1em;
            background-color: transparent;
            color: var(--text-color);
            outline: none;
        }

        #search-input::placeholder {
            color: #999999;
        }

        #search-form button {
            background-color: var(--hover-color);
            color: var(--text-color);
            border: none;
            padding: 0 20px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        #search-form button:hover {
            background-color: #9d50ff;
        }

        /* Link Grid Layout (The Core Professional Structure) */
        .link-grid {
            display: grid;
            /* Creates a responsive grid with columns that are at least 300px wide */
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); 
            gap: 30px;
            max-width: 1300px;
            margin: 0 auto;
        }

        /* Category Box Styling */
        .link-category {
            background-color: var(--card-bg);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s;
        }

        .link-category:hover {
            transform: translateY(-5px); /* Subtle lift on hover */
        }

        .link-category h2 {
            font-size: 1.4em;
            margin-top: 0;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--accent-color);
            color: var(--text-color);
            font-weight: 600;
        }

        .link-category h2 i {
            margin-right: 10px;
            color: var(--hover-color); /* Apply accent color to icons */
        }

        /* Individual Link Card Styling */
        .link-card {
            display: block;
            text-decoration: none;
            color: var(--text-color);
            background-color: var(--accent-color);
            padding: 12px 15px;
            margin-top: 10px;
            border-radius: 8px;
            font-weight: 500;
            transition: background-color 0.3s, transform 0.2s;
        }

        .link-card:hover {
            background-color: var(--hover-color);
            transform: translateX(5px);
        }

        /* Responsive Adjustments for Smaller Screens */
        @media (max-width: 768px) {
            body {
                padding: 15px;
            }
            .link-grid {
                grid-template-columns: 1fr; /* Stack categories on small screens */
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>My Professional Dashboard</h1>
        <p>Your centralized hub for productivity.</p>
    </header>

    <div class="search-container">
        <form id="search-form" action="https://www.google.com/search" method="get">
            <input type="text" id="search-input" name="q" placeholder="Search Google or type a full URL..." required>
            <button type="submit"><i class="fas fa-search"></i></button>
        </form>
    </div>

    <main class="link-grid">
        
        <section class="link-category">
            <h2><i class="fas fa-code"></i> Development Tools</h2>
            <a href="https://github.com/" target="_blank" class="link-card">GitHub</a>
            <a href="https://stackoverflow.com/" target="_blank" class="link-card">Stack Overflow</a>
            <a href="https://developer.mozilla.org/en-US/" target="_blank" class="link-card">MDN Docs</a>
            <a href="https://www.figma.com/" target="_blank" class="link-card">Figma</a>
        </section>

        <section class="link-category">
            <h2><i class="fas fa-globe"></i> News & Tech</h2>
            <a href="https://news.ycombinator.com/" target="_blank" class="link-card">Hacker News</a>
            <a href="https://www.theverge.com/" target="_blank" class="link-card">The Verge</a>
            <a href="https://www.reddit.com/r/programming/" target="_blank" class="link-card">r/programming</a>
            <a href="https://en.wikipedia.org/" target="_blank" class="link-card">Wikipedia</a>
        </section>

        <section class="link-category">
            <h2><i class="fas fa-tasks"></i> Productivity</h2>
            <a href="https://calendar.google.com/" target="_blank" class="link-card">Google Calendar</a>
            <a href="https://trello.com/" target="_blank" class="link-card">Trello</a>
            <a href="https://mail.google.com/" target="_blank" class="link-card">Gmail</a>
            <a href="https://zoom.us/" target="_blank" class="link-card">Zoom</a>
        </section>

        <section class="link-category">
            <h2><i class="fas fa-palette"></i> Design & Utilities</h2>
            <a href="https://unsplash.com/" target="_blank" class="link-card">Unsplash</a>
            <a href="https://fonts.google.com/" target="_blank" class="link-card">Google Fonts</a>
            <a href="https://htmlcolorcodes.com/" target="_blank" class="link-card">Color Picker</a>
            <a href="https://validator.w3.org/" target="_blank" class="link-card">W3C Validator</a>
        </section>
        
        <section class="link-category">
            <h2><i class="fas fa-cloud"></i> Cloud Services</h2>
            <a href="https://aws.amazon.com/" target="_blank" class="link-card">AWS Console</a>
            <a href="https://cloud.google.com/" target="_blank" class="link-card">Google Cloud</a>
            <a href="https://azure.microsoft.com/" target="_blank" class="link-card">Azure Portal</a>
            <a href="https://www.netlify.com/" target="_blank" class="link-card">Netlify</a>
        </section>

    </main>

    <script>
        // JavaScript for smart search bar functionality
        document.addEventListener('DOMContentLoaded', () => {
            const searchForm = document.getElementById('search-form');
            const searchInput = document.getElementById('search-input');

            // Function to check if the input is likely a URL
            const isUrl = (string) => {
                // Checks for a protocol (http/https) or a string followed by a dot (e.g., "google.com")
                const urlPattern = /^(https?:\/\/)?([\w.-]+\.[a-z]{2,})(\S*)$/i;
                return urlPattern.test(string);
            };

            searchForm.addEventListener('submit', (e) => {
                const query = searchInput.value.trim();

                if (query && isUrl(query)) {
                    // If it looks like a URL, prevent the default form submission (Google search)
                    e.preventDefault();
                    
                    // Ensure the URL has a protocol for the browser to navigate correctly
                    let targetUrl = query;
                    if (!targetUrl.match(/^https?:\/\//i)) {
                        targetUrl = 'https://' + targetUrl;
                    }
                    
                    // Navigate to the URL
                    window.location.href = targetUrl;
                }
                // If it's not a URL, the form will submit to Google search automatically (via the HTML 'action' attribute)
            });
        });
    </script>
</body>
</html>
