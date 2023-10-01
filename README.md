<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>R.M. Pfister Interactive ResumeGPT</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
    body {
        font-family: 'Roboto', sans-serif;
        background-color: #2e2e2e;
        display: flex;
        justify-content: center;
        align-items: center;
        min-height: 100vh;
        overflow: hidden;
        background-image: url('computer-frame.png'); /* Replace with your computer frame image */
        background-repeat: no-repeat;
        background-size: cover;
    }
    #screen {
        background-color: #000;
        border: 4px solid #00ff00;
        border-radius: 15px;
        width: 60%;
        height: 80%;
        overflow: auto;
        padding: 20px;
        box-shadow: 0 0 20px rgba(0,255,0,0.5);
        position: relative;
    }
    #buttons div {
        margin: 5px;
        display: inline-block;
    }
    button {
        background-color: #00ff00;
        border: none;
        color: #000;
        padding: 10px 20px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        cursor: pointer;
        border-radius: 12px;
        transition: background-color 0.3s ease;
    }
    button:hover {
        background-color: #008800;
    }
    #typed-output {
        white-space: pre-wrap;
        color: #00ff00;
        position: absolute;
        bottom: 20px;
        width: calc(100% - 40px);
    }
    .glitch {
        position: relative;
        color: white;
    }
    .glitch::before, .glitch::after {
        content: attr(data-text);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: black;
    }
    .glitch::before {
        left: 2px;
        text-shadow: -2px 0 red;
        animation: glitch 0.3s infinite linear alternate-reverse;
    }
    .glitch::after {
        left: -2px;
        text-shadow: -2px 0 blue;
        animation: glitch 0.3s infinite linear alternate;
    }
    @keyframes glitch {
        0% {clip-path: inset(100% 0 1% 0);}
        5% {clip-path: inset(48% 0 52% 0);}
        10% {clip-path: inset(30% 0 20% 0);}
        15% {clip-path: inset(52% 0 48% 0);}
        20% {clip-path: inset(90% 0 10% 0);}
        25% {clip-path: inset(20% 0 30% 0);}
        30% {clip-path: inset(92% 0 1% 0);}
        35% {clip-path: inset(10% 0 20% 0);}
        40% {clip-path: inset(73% 0 14% 0);}
        45% {clip-path: inset(40% 0 30% 0);}
        50% {clip-path: inset(60% 0 40% 0);}
        55% {clip-path: inset(100% 0 1% 0);}
        60% {clip-path: inset(30% 0 40% 0);}
        65% {clip-path: inset(100% 0 1% 0);}
        70% {clip-path: inset(20% 0 10% 0);}
        75% {clip-path: inset(80% 0 20% 0);}
        80% {clip-path: inset(100% 0 1% 0);}
        85% {clip-path: inset(10% 0 20% 0);}
        90% {clip-path: inset(100% 0 1% 0);}
        95% {clip-path: inset(20% 0 30% 0);}
        100% {clip-path: inset(70% 0 20% 0);}
    }
</style>
</head>
<body>
<div id="screen">
    <div class="glitch" data-text="R.M. Pfister Interactive ResumeGPT" style="font-size: 2em; text-align: center; margin-bottom: 20px;">R.M. Pfister Interactive ResumeGPT</div>
    <div id="buttons">
        <div><button onclick="displaySection('summary')">Professional Summary</button></div>
        <div><button onclick="displaySection('experience')">Work Experience</button></div>
        <div><button onclick="displaySection('education')">Education</button></div>
        <div><button onclick="displaySection('analysis')">Subject Analysis</button></div>
    </div>
    <div id="typed-output"></div>
</div>
<script src="https://cdn.jsdelivr.net/npm/typed.js@2.0.12"></script>
<script>
    function displaySection(section) {
        document.getElementById('typed-output').innerHTML = ''; // Clear previous content
        let options = {
            strings: [getSectionContent(section)],
            typeSpeed: 50,
            showCursor: false,
        };
        new Typed('#typed-output', options);
    }

    function getSectionContent(section) {
        switch(section) {
            case 'summary':
                return `Multifaceted professional with an extensive background in welding, fabrication, and instructional roles, complemented by a profound engagement in blockchain, cryptocurrency, and NFT domains. Proficient in graphic design, audio production, podcasting, and AI, with substantial experience beta testing emerging technologies. Founder of initiatives focused on advancing human development through large language models and blockchain technologies.`;
            case 'experience':
                return `Founder and Host, Web3Radio – [Location]\nMay 2022 – Present\nEstablished a podcast and X Space focusing on music, decentralization, NFTs, and cryptocurrencies. Hosted numerous episodes discussing the latest trends and developments in the blockchain space.`; // Add the rest of your work experience here
            case 'education':
                return `Associate in Applied Science\nIvy Tech Community College – Terre Haute, IN\nDecember 2015 – October 2019\n\nTechnical Certificate in Industrial Technology\nIvy Tech Community College – Terre Haute, IN\nDecember 2015\n\nCertificate in Structural Welding\nIvy Tech Community College – Terre Haute, IN\nMay 2015`;
            case 'analysis':
                return `Subject Analysis\n\nGenerative AI:\nGiven your extensive engagement in beta testing various AI technologies, your aptitude for generative AI is apparent. Your practical experience with AI platforms, coupled with your diverse skill set in welding, teaching, and blockchain technology, positions you uniquely in the job market. Your cross-disciplinary expertise is a strong asset, and your continuous learning attitude enhances your potential in the AI domain significantly.`;
            default:
                return '';
        }
    }
</script>
</body>
</html>
```

<!---
VRSEx/VRSEx is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
