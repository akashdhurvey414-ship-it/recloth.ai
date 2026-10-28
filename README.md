# recloth.ai
A sustainable clothing reuse and recycling project.
ReCloth AI ♻️

A Sustainable Clothing Reuse and Recycling Project

ReCloth is a sustainability-focused web project designed to help people find creative ways to reuse old and unused clothes instead of throwing them away.

Key Features

- Upload a clothing image.
- Select clothing type and condition.
- Explore possible reuse ideas for old clothes.
- Encourage clothing donation, recycling and exchange.

Project Goal

To reduce textile waste and promote sustainable living through technology.

Technologies

HTML, CSS, JavaScript and an AI-based image-processing experiment using Transformers.js.

Project Links

- Live Demo: [https://recloth.odoo.com/ ]
- GitHub Repository: [https://github.com/akashdhurvey414-ship-it/recloth.ai]

Team

Add your team members and clearly mention each person's contribution.

Project status: Add the features that are currently working and describe any features still under development. 

html code of ai cam : Hugging Face's logo
Hugging Face
Models
Datasets
Spaces
Docs
Pricing


Hugging Face is way more fun with friends and colleagues! 🤗 Join an organization
Spaces:
dhurveyam
/
recloth-vision 

Like
0
App
Files
Community
Settings
recloth-vision
/
index.html 
dhurveyam's picture
dhurveyam
Update index.html
2397681
verified
8 days ago

Download
Raw
History
Blame
Edit
Delete
2.65 kB

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#176b4d">
  <title>ReCloth AI | Give Clothes a Second Life</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header class="topbar">
    <a class="brand" href="#" aria-label="ReCloth home">
      <span class="logo">♻</span> ReCloth
    </a>
    <span class="tag">Sustainable Living</span>
  </header>

  <main class="main">
    <section class="intro">
      <p class="eyebrow">REUSE • REIMAGINE • RECYCLE</p>
      <h1>Give Your Clothes a <span>Second Life</span></h1>
      <p>Upload a photo of unused clothing and discover creative ways to reuse it.</p>
    </section>

    <section class="tool-card">
      <label class="upload-area" for="upload">
        <span class="upload-icon">↑</span>
        <strong>Upload your clothing photo</strong>
        <span>Tap to choose a photo or take one with your camera</span>
        <span class="small">JPG, PNG or WEBP</span>
      </label>

      <input id="upload" type="file" accept="image/*" capture="environment">

      <div id="preview-wrap" class="preview-wrap hidden">
        <img id="preview" alt="Your uploaded clothing">
        <button id="remove" class="text-button" type="button">Remove photo</button>
      </div>

      <label class="field-label" for="cloth-type">What type of clothing is it?</label>
      <select id="cloth-type">
        <option value="tshirt">Old T-shirt</option>
        <option value="jeans">Old jeans / denim</option>
        <option value="shirt">Old shirt</option>
        <option value="saree">Saree or dupatta</option>
        <option value="towel">Old towel</option>
        <option value="sweater">Old sweater</option>
        <option value="bedsheet">Old bedsheet</option>
        <option value="other">Other fabric</option>
      </select>

      <button id="analyze" class="primary-button" type="button" disabled>
        Find Reuse Ideas
      </button>

      <p id="status" class="status" role="status" aria-live="polite">
        Upload a photo to get started.
      </p>

      <section id="results" class="results hidden" aria-live="polite">
        <h2>Your ReCloth Ideas</h2>
        <p id="prediction" class="prediction"></p>
        <div id="ideas" class="ideas"></div>
        <p class="note">Suggestions are ideas for reuse, not a guarantee of fabric suitability.</p>
      </section>
    </section>

    <p class="footer">Small changes, less textile waste. 💚</p>
  </main>

  <script type="module" src="index.js"></script>
</body>
</html>


