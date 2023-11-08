- 👋 Hi, I’m @Saiidhassou
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Saiidhassou/Saiidhassou is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
console.log('Hello!');
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SocialFinder</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Your website content goes here -->
    <h1>Welcome to SocialFinder!</h1>

    <script src="script.js"></script>
</body>
</html>
/* styles.css */
body {
    background-color: #f8f8f8;
    color: #333333;
}

h1 {
    color: #ff5500;
}<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SocialFinder</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav>
            <h1>SocialFinder</h1>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Search</a></li>
                <li><a href="#">Profile</a></li>
                <li><a href="#">Settings</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Your content goes here -->
    </main>

    <footer>
        <p>&copy; 2022 SocialFinder. All rights reserved.</p>
    </footer>

    <script src="app.js"></script>
</body>
</html>
/* styles.css */
body {
    margin: 0;
    padding: 0;
    font-family: Arial, sans-serif;
    background-color: #f8f8f8;
    color: #333333;
}

header {
    background-color: #ff5500;
    padding: 20px;
    color: #ffffff;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

nav h1 {
    font-size: 24px;
}

nav ul {
    list-style-type: none;
}

nav ul li {
    display: inline-block;
    margin-right: 10px;
}

nav ul li a {
    color: #ffffff;
    text-decoration: none;
}

main {
    padding: 20px;
}

footer {
    background-color: #dddddd;
    padding: 10px;
    text-align: center;
}
// app.js
// Add your JavaScript code here

// Get DOM elements
const homeLink = document.querySelector('nav ul li:nth-child(1) a');
const searchLink = document.querySelector('nav ul li:nth-child(2) a');
const profileLink = document.querySelector('nav ul li:nth-child(3) a');
const settingsLink = document.querySelector('nav ul li:nth-child(4) a');
const mainContent = document.querySelector('main');

// Event listeners for navigation links
homeLink.addEventListener('click', () => {
    setActiveLink('home');
    showHomePage();
});

searchLink.addEventListener('click', () => {
    setActiveLink('search');
    showSearchPage();
});

profileLink.addEventListener('click', () => {
    setActiveLink('profile');
    showProfilePage();
});

settingsLink.addEventListener('click', () => {
    setActiveLink('settings');
    showSettingsPage();
});

// Function to set active navigation link
function setActiveLink(activePage) {
    const links = [homeLink, searchLink, profileLink, settingsLink];
    links.forEach(link => {
        if (link.classList.contains('active')) {
            link.classList.remove('active');
        }
    });

    switch (activePage) {
        case 'home':
            homeLink.classList.add('active');
            break;
        case 'search':
            searchLink.classList.add('active');
            break;
        case 'profile':
            profileLink.classList.add('active');
            break;
        case 'settings':
            settingsLink.classList.add('active');
            break;
        default:
            break;
    }
}

// Functions to show different pages
function showHomePage() {
    mainContent.innerHTML = '<h2>Welcome to the Home Page!</h2>';
}

function showSearchPage() {
    mainContent.innerHTML = '<h2>Search for Friends and Connections</h2>';
}

function showProfilePage() {
    mainContent.innerHTML = '<h2>View and Edit Your Profile</h2>';
}

function showSettingsPage() {
    mainContent.innerHTML = '<h2>Customize Your SocialFinder Experience</h2>';
}

// Initial page load
showHomePage();
