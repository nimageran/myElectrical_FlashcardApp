# Nima Flashcards — README
**Note:** Edit the Excel file inside the Excel folder, as it is not possible to make some changes, like highlighting, in CSV. After editing the Excel, save it as CSV and replace the CSV file inside the asset folder.


Nima's Flashcards – User Guide1. The Basic ConceptThis tool is a single HTML file. You do not need to install software or use a server. When you open the file in Chrome or Safari, it looks into your local folders to find your questions (CSV) and your pictures (Images).2. Folder StructureYou must organize your files exactly like this for the code to find them:/Project_Folder
│
├── index.html          <-- The code file (Open this to start)
├── README.md           <-- This help file
│
└── assets/             <-- Main data folder
    ├── cards.csv       <-- Your list of questions
    └── images/         <-- Folder where you dump all pictures
        ├── card1.png
        ├── Fcard1.png
        └── ...
3. How to Add ImagesThe code matches images to cards based on the ID you wrote in your CSV file. It supports .jpg, .png, and .webp.The "F" RuleBack Image (Answer): Name the image exactly the same as the ID.Example: If ID is card10, name the image card10.png.Front Image (Question): Add a capital F to the start of the filename.Example: If ID is card10, name the image Fcard10.png.4. The CSV File FormatYour assets/cards.csv file needs three columns. The first row must be the header.Example Content:id,front,back
card1,What is this symbol?,Resistor
card2,Calculate the voltage,12V
id: A unique name (e.g., card1). This connects the text to the image.front: The question text.back: The answer text.5. How the Logic WorksLoading: When you open index.html, it reads cards.csv.Front: When a card appears, it looks for an image named F + ID (e.g., Fcard1.png). If found, it shows it above the question.Back: When you tap "Flip," it hides the front image and looks for the standard ID image (e.g., card1.png) to show with the answer.
