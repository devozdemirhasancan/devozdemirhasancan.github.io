<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hasancan | Developer</title>
    <meta name="description" content="Hasancan - Full Stack Developer working with AI, Web, and Embedded Systems.">
    <meta name="keywords" content="Hasancan, Developer, Full Stack, AI, Embedded Systems, Web Development">
    <meta name="author" content="Hasancan">
    <meta property="og:title" content="Hasancan | Developer">
    <meta property="og:description" content="Full Stack Developer working with AI, Web, and Embedded Systems.">
    <meta property="og:image" content="https://sanaticinhasancan.art">
    <meta property="og:url" content="https://sanaticinhasancan.art">
    <meta name="twitter:card" content="summary_large_image">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #121212;
            color: #ffffff;
            text-align: center;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
        }
        h1 {
            font-size: 2.5rem;
        }
        p {
            font-size: 1.2rem;
        }
        .socials a {
            color: #ffffff;
            margin: 10px;
            font-size: 1.5rem;
            text-decoration: none;
        }
        .projects {
            margin-top: 30px;
        }
        .project-card {
            background: #1e1e1e;
            padding: 15px;
            border-radius: 10px;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Hey there! 👋 I'm Hasan Can</h1>
        <p>Full + Full Stack Developer | AI, Web & Embedded Systems</p>
        
        <div class="socials">
            <a href="https://twitter.com/sanaticincan" target="_blank"><i class="fab fa-twitter"></i></a>
            <a href="mailto:devozdemirhasancan@gmail.com"><i class="fas fa-envelope"></i></a>
            <a href="https://sanaticinhasancan.art" target="_blank"><i class="fas fa-globe"></i></a>
            <a href="https://kick.com/sanaticinhasancan" target="_blank"><i class="fab fa-kickstarter"></i></a>
            <a href="https://instagram.com/sanaticinhasancan" target="_blank"><i class="fab fa-instagram"></i></a>
        </div>
        
        <div class="projects">
            <h2>Projects</h2>
            <div id="repo-list">Loading repositories...</div>
        </div>
    </div>

    <script>
        async function fetchRepos() {
            const username = "devozdemirhasancan";
            const response = await fetch(`https://api.github.com/users/${username}/repos`);
            const repos = await response.json();
            const repoList = document.getElementById("repo-list");
            repoList.innerHTML = "";
            
            repos.forEach(repo => {
                const repoItem = document.createElement("div");
                repoItem.className = "project-card";
                repoItem.innerHTML = `<a href="${repo.html_url}" target="_blank">${repo.name}</a> - ⭐ ${repo.stargazers_count}`;
                repoList.appendChild(repoItem);
            });
        }

        fetchRepos();
    </script>
</body>
</html>
