/* Data Architecture Matrix for Classes 6-12 */
const academicMatrix = {
  // Lower Secondary (6-8)
  "6": {
    "Science": ["Components of Food", "Sorting Materials into Groups", "Separation of Substances", "Getting to Know Plants", "Motion and Measurement"],
    "Mathematics": ["Knowing Our Numbers", "Whole Numbers", "Playing with Numbers", "Basic Geometrical Ideas"],
    "English": ["A Different Kind of School", "Who I Am", "Fair Play"],
    "Hindi": ["वह चिड़िया जो", "बचपन", "नादान दोस्त"]
  },
  "8": {
    "Science": ["Crop Production and Management", "Microorganisms", "Coal and Petroleum", "Combustion and Flame"],
    "Mathematics": ["Rational Numbers", "Linear Equations in One Variable", "Understanding Quadrilaterals"],
    "English": ["The Best Christmas Present in the World", "Tsunami"],
    "Hindi": ["दीवानों की हस्ती", "भगवान के डाकिए"]
  },

  // Secondary Foundation (9-10)
  "10": {
    "Science": ["Chemical Reactions and Equations", "Acids, Bases and Salts", "Metals and Non-metals", "Carbon and Its Compounds", "Life Processes", "Light - Reflection"],
    "Mathematics": ["Real Numbers", "Polynomials", "Pair of Linear Equations", "Quadratic Equations", "Triangles"],
    "Social Science": ["The Rise of Nationalism in Europe", "Resources and Development", "Power Sharing"],
    "English": ["A Letter to God", "Nelson Mandela: Long Walk to Freedom"],
    "Hindi Course A": ["नेताजी का चश्मा", "बालगोबिन भगत", "सूरदास के पद"]
  },

  // Senior Secondary Streams (11-12)
  "12": {
    "Physics": ["Electric Charges and Fields", "Electrostatic Potential", "Current Electricity", "Moving Charges and Magnetism"],
    "Chemistry": ["Solutions", "Electrochemistry", "Chemical Kinetics", "The d- and f-Block Elements"],
    "Biology": ["Sexual Reproduction in Flowering Plants", "Human Reproduction", "Principles of Inheritance"],
    "Accountancy": ["Accounting for Partnership Firms", "Company Accounts", "Financial Statements"],
    "Business Studies": ["Nature and Significance of Management", "Principles of Management", "Business Environment"],
    "Economics": ["National Income and Related Aggregates", "Money and Banking", "Government Budget"],
    "English Core": ["The Last Lesson", "Lost Spring", "Deep Water", "My Mother at Sixty-six"],
    "Hindi Core": ["आत्मपरिचय", "पतंग", "भक्तिन"]
  }
};

/* Tab Navigation Handler */
function switchTab(tabId) {
  const tabs = document.querySelectorAll('.tab-content');
  const buttons = document.querySelectorAll('.tab-btn');

  tabs.forEach(tab => tab.style.display = 'none');
  buttons.forEach(btn => btn.classList.remove('active'));

  document.getElementById(tabId).style.display = 'block';
  event.currentTarget.classList.add('active');
}

/* Dynamic Cascading Dropdown Functions */
function loadNotesSubjects() {
  const selectedClass = document.getElementById("notesClass").value;
  const subjectSelect = document.getElementById("notesSubject");
  subjectSelect.innerHTML = "<option value=''>Select Subject</option>";
  
  if (academicMatrix[selectedClass]) {
    Object.keys(academicMatrix[selectedClass]).forEach(sub => {
      let opt = document.createElement("option");
      opt.value = sub;
      opt.textContent = sub;
      subjectSelect.appendChild(opt);
    });
  }
}

function loadNotesChapters() {
  const selectedClass = document.getElementById("notesClass").value;
  const selectedSubject = document.getElementById("notesSubject").value;
  const chapterSelect = document.getElementById("notesChapter");
  chapterSelect.innerHTML = "<option value=''>Select Chapter</option>";

  if (academicMatrix[selectedClass] && academicMatrix[selectedClass][selectedSubject]) {
    academicMatrix[selectedClass][selectedSubject].forEach(chap => {
      let opt = document.createElement("option");
      opt.value = chap;
      opt.textContent = chap;
      chapterSelect.appendChild(opt);
    });
  }
}

/* Chapter Revision Notes Generator */
function generateChapterNotes() {
  const cls = document.getElementById("notesClass").value;
  const sub = document.getElementById("notesSubject").value;
  const chap = document.getElementById("notesChapter").value;
  
  if (!cls || !sub || !chap) {
    alert("Please select Class, Subject, and Chapter first.");
    return;
  }

  const outputContainer = document.getElementById("notesOutput");
  const contentArea = document.getElementById("notesContent");
  outputContainer.style.display = "block";

  contentArea.innerHTML = `
    <div class="note-paper">
      <div style="border-bottom: 2px solid #1a73e8; padding-bottom: 10px; margin-bottom: 15px;">
        <h2 style="margin: 0; color: #1a73e8;">Class ${cls} ${sub} Revision Notes</h2>
        <h3 style="margin: 5px 0 0 0; color: #5f6368;">Chapter: ${chap}</h3>
      </div>

      <div>
        <h4>📌 Important Definitions & Core Concepts</h4>
        <ul>
          <li><strong>Primary Framework:</strong> Detailed explanation covering NCERT principles for ${chap}.</li>
          <li><strong>Fundamental Rule:</strong> Key assumptions, theories, or historical context governing this chapter.</li>
        </ul>
      </div>

      <div class="formula-box">
        <h4 style="margin-top: 0;">⚡ Essential Formulae / Key Vocabulary</h4>
        <p>• Term / Equation 1: Primary relationship or definition.</p>
        <p>• Term / Equation 2: Secondary derivation or rule.</p>
      </div>

      <div>
        <h4>🔥 Expected Board & School Exam Questions</h4>
        <ul>
          <li><strong>2-Mark Question:</strong> Define the core properties of ${chap}.</li>
          <li><strong>5-Mark Question:</strong> Explain the full mechanism/process with neat labelled diagrammatic steps.</li>
        </ul>
      </div>
    </div>
  `;
}

/* Solution Resolver Simulation */
function generateSolution() {
  const question = document.getElementById("userQuestion").value.trim();
  
  if (!question) {
    alert("Please enter or paste a question to solve.");
    return;
  }

  const solutionOutput = document.getElementById("solutionOutput");
  const solutionText = document.getElementById("solutionText");
  solutionOutput.style.display = "block";

  solutionText.innerHTML = `
    <p><strong>Question:</strong> "${question}"</p>
    <hr style="border: 0.5px solid #dadce0;">
    <h4>CBSE Marking Scheme Solution:</h4>
    <p><strong>Step 1 (Given & Concept):</strong> Identify the core parameters and governing NCERT principle [1 Mark].</p>
    <p><strong>Step 2 (Execution/Derivation):</strong> Apply standard formula or logical steps step-by-step [2 Marks].</p>
    <p><strong>Step 3 (Final Answer):</strong> Conclude with exact units/summary statement [1 Mark].</p>
  `;
}
