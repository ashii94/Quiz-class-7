<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>AI Assessment | Raasti Class 7</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Google Fonts for Beautiful Typography -->
  <link href="https://fonts.googleapis.com/css2?family=Fredoka:wght@700&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --primary: #ff6f61;
      --secondary: #6ec6ff;
      --accent1: #ffd600;
      --accent2: #6fffbf;
      --accent3: #b388ff;
      --accent4: #ff8a80;
      --background: #fffdea;
      --box-border: #3e2723;
    }
    body {
      margin: 0;
      font-family: 'Montserrat', Arial, sans-serif;
      background: var(--background);
      min-height: 100vh;
    }
    .theme-page {
      background: radial-gradient(circle at 50% 40%, #ffd600 0%, #6ec6ff 60%, #fffdea 100%);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      color: #3e2723;
      position: relative;
      overflow: hidden;
    }
    .bubble {
      position: absolute;
      border-radius: 50%;
      opacity: 0.2;
      z-index: 0;
      pointer-events: none;
    }
    .bubble1 { width: 300px; height: 300px; top: 10%; left: 5%; background: var(--accent1);}
    .bubble2 { width: 200px; height: 200px; bottom: 10%; right: 8%; background: var(--accent2);}
    .bubble3 { width: 120px; height: 120px; top: 70%; left: 70%; background: var(--accent3);}
    .bubble4 { width: 180px; height: 180px; bottom: 20%; left: 18%; background: var(--accent4);}
    .theme-title {
      font-family: 'Fredoka', cursive;
      font-size: 3.2rem;
      letter-spacing: 2px;
      margin-bottom: 0.6em;
      color: #fff;
      text-shadow: 0 3px 14px #ff6f6170, 0 0 1px #3e2723;
      position: relative;
      z-index: 1;
    }
    .theme-subtitle {
      font-size: 1.4rem;
      margin-bottom: 2.2em;
      background: #fff9;
      padding: 0.8em 2.5em;
      border-radius: 24px;
      display: inline-block;
      font-weight: bold;
      box-shadow: 0 2px 8px #ffd60033;
      position: relative;
      z-index: 1;
    }
    .robot-img {
      width: 130px;
      margin-bottom: 2em;
      filter: drop-shadow(0 8px 12px #6ec6ff55);
      position: relative;
      z-index: 1;
    }
    .styled-btn {
      font-family: 'Fredoka', cursive;
      background: linear-gradient(90deg, #ffd600 30%, #ff6f61 80%);
      color: #3e2723;
      border: none;
      border-radius: 50px;
      font-size: 1.6rem;
      font-weight: bold;
      padding: 1em 3em;
      cursor: pointer;
      box-shadow: 0 4px 24px #ff6f6136;
      transition: transform 0.1s, box-shadow 0.2s;
      margin-top: 1.7em;
      position: relative;
      z-index: 1;
    }
    .styled-btn:hover {
      transform: scale(1.08);
      box-shadow: 0 8px 30px #ff6f6140;
      background: linear-gradient(90deg, #ff6f61 30%, #ffd600 100%);
    }
    /* Assessment Page Styles */
    .assessment-page {
      padding: 0;
      background: repeating-linear-gradient(
        135deg,
        #fffdea 0 40px,
        #ffecb3 40px 60px,
        #e1f5fe 60px 100px,
        #fffdea 100px 140px
      );
      min-height: 100vh;
      min-width: 100vw;
      position: relative;
    }
    .upper-space {
      background: linear-gradient(90deg, #ff8a80 0%, #ffd600 70%, #b388ff 100%);
      min-height: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      box-shadow: 0 10px 30px #ffb30022;
    }
    .assessment-title {
      font-size: 2.2rem;
      font-family: 'Fredoka', cursive;
      text-align: center;
      margin: 1.5em 0 0.8em 0;
      color: #3e2723;
      letter-spacing: 1px;
      text-shadow: 0 2px 8px #ffd60033;
    }
    .timers {
      display: flex;
      justify-content: center;
      gap: 2em;
      margin-bottom: 1.1em;
      margin-top: 1.1em;
    }
    .timer-box {
      background: #fff6;
      border-radius: 16px;
      padding: 0.7em 1.4em;
      font-weight: bold;
      font-size: 1.15em;
      color: #3e2723;
      box-shadow: 0 1px 8px #ff6f6120;
      display: flex;
      align-items: center;
      gap: 0.5em;
    }
    .timer-icon {
      width: 1.3em;
      height: 1.3em;
      vertical-align: middle;
      margin-right: 0.2em;
      filter: drop-shadow(0 1px 2px #ff6f6111);
    }
    form {
      max-width: 680px;
      margin: auto;
      background: #fff;
      padding: 2.3em 2.5em 1.4em 2.5em;
      border-radius: 32px;
      box-shadow: 0 8px 38px #ff6f611b;
      margin-bottom: 3em;
    }
    .section-label {
      margin: 2em 0 1em 0;
      font-size: 1.18em;
      font-weight: bold;
      background: linear-gradient(90deg, #6ec6ff, #ffd600, #b388ff);
      padding: 0.5em 1.4em;
      border-radius: 15px;
      display: inline-block;
      color: #3e2723;
      margin-bottom: 1.35em;
      box-shadow: 0 0 10px #ff6f6132;
    }
    .mcq {
      margin: 0.9em 0;
      background: linear-gradient(90deg, #fffdea 90%, #ffecb3 100%);
      padding: 1.2em 1.3em;
      border-radius: 18px;
      border: 2.5px solid var(--secondary);
      box-shadow: 0 2px 14px #6ec6ff10;
      transition: box-shadow 0.2s;
    }
    .mcq-title {
      font-weight: bold;
      margin-bottom: 0.6em;
      color: #22223b;
    }
    .mcq-options label {
      display: block;
      margin-bottom: 0.3em;
      cursor: pointer;
      padding-left: 0.7em;
      transition: background 0.1s;
    }
    .mcq-options input[type="radio"] {
      margin-right: 0.7em;
      accent-color: var(--primary);
    }
    .short-answer {
      margin-bottom: 1.3em;
    }
    .short-answer input, .short-answer textarea {
      width: 100%;
      font-size: 1em;
      padding: 0.8em;
      border-radius: 11px;
      border: 2px solid #ffd600;
      background: #fffde7;
      margin-top: 0.5em;
      font-family: inherit;
      box-shadow: 0 1px 6px #ff6f610a;
      resize: vertical;
      min-height: 35px;
      max-height: 90px;
    }
    .short-answer textarea {
      min-height: 50px;
    }
    .submit-btn {
      display: block;
      font-family: 'Fredoka', cursive;
      background: linear-gradient(95deg, #ff6f61, #ffd600);
      color: #3e2723;
      border: none;
      border-radius: 40px;
      font-size: 1.3rem;
      font-weight: bold;
      padding: 0.8em 2.7em;
      cursor: pointer;
      margin: 2.3em auto 1.1em auto;
      box-shadow: 0 6px 24px #ffd60044;
      transition: transform 0.1s, box-shadow 0.2s;
    }
    .submit-btn:hover {
      transform: scale(1.07);
      box-shadow: 0 8px 36px #ffd60055;
      background: linear-gradient(95deg, #ffd600, #ff6f61);
    }
    /* Result Modal */
    .result-modal {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(255, 223, 186, 0.82);
      z-index: 99;
      display: flex;
      align-items: center;
      justify-content: center;
      visibility: hidden;
      opacity: 0;
      transition: opacity 0.25s;
    }
    .result-modal.show {
      visibility: visible;
      opacity: 1;
    }
    .result-content {
      background: linear-gradient(120deg, #fffde7 60%, #ffd600 100%);
      border-radius: 28px;
      padding: 2.8em 2.2em 2.2em 2.2em;
      text-align: center;
      position: relative;
      min-width: 320px;
      box-shadow: 0 12px 54px #ff6f6128;
      animation: popin 0.7s cubic-bezier(.6,-0.28,.74,.05) 1;
    }
    @keyframes popin {
      0% { transform: scale(0.6); opacity: 0; }
      88% { transform: scale(1.09); opacity: 1; }
      100% { transform: scale(1); }
    }
    .result-robot {
      width: 128px;
      margin-bottom: 1em;
      animation: bounce 1.5s infinite;
    }
    @keyframes bounce {
      0%,100% { transform: translateY(0);}
      50% { transform: translateY(-13px);}
    }
    .result-title {
      font-size: 2.25em;
      font-family: 'Fredoka', cursive;
      margin-bottom: 0.2em;
      color: #ff6f61;
      text-shadow: 0 2px 14px #ffd60033;
    }
    .result-score {
      font-size: 1.13em;
      font-weight: bold;
      margin-bottom: 1em;
      color: #22223b;
    }
    .result-msg {
      font-size: 1.3em;
      margin-bottom: 0.7em;
      color: #3e2723;
    }
    .close-btn {
      margin-top: 1.7em;
      background: #ffd600;
      color: #ff6f61;
      border-radius: 20px;
      border: none;
      padding: 0.6em 2em;
      font-size: 1.1em;
      font-weight: bold;
      cursor: pointer;
      box-shadow: 0 2px 11px #ffd60033;
      transition: background 0.15s, color 0.15s;
    }
    .close-btn:hover {
      background: #ff6f61;
      color: #ffd600;
    }
    @media (max-width: 700px) {
      form { padding: 1.2em 0.5em;}
      .assessment-title { font-size:1.3em;}
      .theme-title { font-size:1.5em;}
      .upper-space { min-height:50px;}
    }
  </style>
</head>
<body>
  <!-- First Page: Welcome / Theme -->
  <div class="theme-page" id="welcomePage">
    <div class="bubble bubble1"></div>
    <div class="bubble bubble2"></div>
    <div class="bubble bubble3"></div>
    <div class="bubble bubble4"></div>
    <img class="robot-img" src="https://cdn.pixabay.com/photo/2017/01/31/13/14/robot-2027195_960_720.png" alt="Robot Cartoon">
    <div class="theme-title">Artificial Intelligence</div>
    <div class="theme-subtitle">Assessment &mdash; Raasti Class 7</div>
    <button class="styled-btn" onclick="showAssessment()">Start Assessment</button>
  </div>
  <!-- Second Page: Assessment -->
  <div class="assessment-page" id="assessmentPage" style="display:none;">
    <div class="upper-space">
      <div style="width:100%; text-align:center; font-family:'Fredoka', cursive; font-weight:bold; color:#fff; font-size:1.4em; letter-spacing:1px;">AI Assessment</div>
    </div>
    <div class="assessment-title">Artificial Intelligence Assessment <br>Raasti Class 7</div>
    <div class="timers">
      <div class="timer-box">
        <svg class="timer-icon" fill="#ff6f61" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10" stroke="#ff6f61" stroke-width="2" fill="none"/><rect x="11" y="6" width="2" height="7" rx="1" fill="#ff6f61"/><circle cx="12" cy="17" r="1" fill="#ff6f61"/></svg>
        <span id="mcq-timer">10:00</span> MCQs
      </div>
      <div class="timer-box">
        <svg class="timer-icon" fill="#ffd600" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><circle cx="12" cy="12" r="10" stroke="#ffd600" stroke-width="2" fill="none"/><rect x="11" y="6" width="2" height="7" rx="1" fill="#ffd600"/><circle cx="12" cy="17" r="1" fill="#ffd600"/></svg>
        <span id="total-timer">30:00</span> Total
      </div>
    </div>
    <form id="assessmentForm" autocomplete="off">
      <div class="section-label">Section A: Multiple Choice Questions (10 × 1 mark = 10 marks)</div>
      <!-- MCQs -->
      <div class="mcq">
        <div class="mcq-title">1. Which of the following best defines Artificial Intelligence?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q1" value="a"> a) A robot that talks to you</label>
          <label><input type="radio" name="q1" value="b"> b) A program that can solve problems and learn like humans</label>
          <label><input type="radio" name="q1" value="c"> c) Any software on a computer</label>
          <label><input type="radio" name="q1" value="d"> d) A machine with buttons and lights</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">2. One key difference between traditional programming and AI is:</div>
        <div class="mcq-options">
          <label><input type="radio" name="q2" value="a"> a) AI doesn't need electricity</label>
          <label><input type="radio" name="q2" value="b"> b) Traditional programs are used only in banks</label>
          <label><input type="radio" name="q2" value="c"> c) AI learns from data; traditional programming follows fixed rules</label>
          <label><input type="radio" name="q2" value="d"> d) Traditional programming uses robots</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">3. Which example shows AI making a decision based on past experience?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q3" value="a"> a) A light turning on when you flip the switch</label>
          <label><input type="radio" name="q3" value="b"> b) A calculator solving 2 + 2</label>
          <label><input type="radio" name="q3" value="c"> c) YouTube recommending videos based on what you watched</label>
          <label><input type="radio" name="q3" value="d"> d) A microwave heating food</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">4. Why is data important for AI?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q4" value="a"> a) It decorates the program</label>
          <label><input type="radio" name="q4" value="b"> b) Data helps AI machines look good</label>
          <label><input type="radio" name="q4" value="c"> c) AI uses data to learn patterns and improve performance</label>
          <label><input type="radio" name="q4" value="d"> d) It helps make the computer lighter</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">5. Which of these is NOT a correct match of AI application and its use?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q5" value="a"> a) Chatbots – Customer service</label>
          <label><input type="radio" name="q5" value="b"> b) Self-driving car – Road safety</label>
          <label><input type="radio" name="q5" value="c"> c) AI in education – Automatic homework</label>
          <label><input type="radio" name="q5" value="d"> d) AI in healthcare – Disease detection</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">6. AI is considered “artificial” because:</div>
        <div class="mcq-options">
          <label><input type="radio" name="q6" value="a"> a) It works faster than humans</label>
          <label><input type="radio" name="q6" value="b"> b) It’s made by humans, not natural like the brain</label>
          <label><input type="radio" name="q6" value="c"> c) It can run on electricity</label>
          <label><input type="radio" name="q6" value="d"> d) It talks like a robot</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">7. Why should students start learning about AI at a young age?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q7" value="a"> a) So they can become scientists right away</label>
          <label><input type="radio" name="q7" value="b"> b) To play better games</label>
          <label><input type="radio" name="q7" value="c"> c) To understand how smart systems work and prepare for the future</label>
          <label><input type="radio" name="q7" value="d"> d) To avoid doing homework manually</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">8. What would likely happen if an AI system was trained with wrong or biased data?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q8" value="a"> a) It would work perfectly</label>
          <label><input type="radio" name="q8" value="b"> b) It would forget its programming</label>
          <label><input type="radio" name="q8" value="c"> c) It might make unfair or incorrect decisions</label>
          <label><input type="radio" name="q8" value="d"> d) It would become faster</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">9. How is AI different from human intelligence?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q9" value="a"> a) AI needs food to run</label>
          <label><input type="radio" name="q9" value="b"> b) AI uses emotions</label>
          <label><input type="radio" name="q9" value="c"> c) AI learns from data, not feelings or experience</label>
          <label><input type="radio" name="q9" value="d"> d) AI can never make mistakes</label>
        </div>
      </div>
      <div class="mcq">
        <div class="mcq-title">10. Which of the following steps is part of the AI learning process?</div>
        <div class="mcq-options">
          <label><input type="radio" name="q10" value="a"> a) Buying a new computer</label>
          <label><input type="radio" name="q10" value="b"> b) Collecting and cleaning data</label>
          <label><input type="radio" name="q10" value="c"> c) Turning off the device</label>
          <label><input type="radio" name="q10" value="d"> d) Charging the battery</label>
        </div>
      </div>

      <div class="section-label">Section B: Answer the Following (5 × 2 marks = 10 marks)</div>
      <div class="short-answer">
        <label>1. What is Artificial Intelligence in simple words?
          <input type="text" name="b1" maxlength="120" required>
        </label>
      </div>
      <div class="short-answer">
        <label>2. Give two examples of AI in daily life.
          <input type="text" name="b2" maxlength="120" required>
        </label>
      </div>
      <div class="short-answer">
        <label>3. Why is AI important in today’s world?
          <input type="text" name="b3" maxlength="120" required>
        </label>
      </div>
      <div class="short-answer">
        <label>4. Mention any two fields where AI is used.
          <input type="text" name="b4" maxlength="120" required>
        </label>
      </div>
      <div class="short-answer">
        <label>5. Name one advantage and one challenge of AI.
          <input type="text" name="b5" maxlength="120" required>
        </label>
      </div>

      <div class="section-label">Section C: Conceptual Question (1 × 5 marks = 5 marks)</div>
      <div class="short-answer">
        <label>
          Q: Explain how AI works using a simple example, starting from data collection to giving a result.
          <textarea name="c1" rows="4" maxlength="350" required placeholder="E.g., How AI helps find a cat in a photo..."></textarea>
        </label>
      </div>

      <button class="submit-btn" type="submit">Submit</button>
    </form>
  </div>
  <!-- Result Modal -->
  <div class="result-modal" id="resultModal">
    <div class="result-content">
      <img class="result-robot" id="resultRobot" src="https://cdn.pixabay.com/photo/2017/01/31/13/14/robot-2027195_960_720.png" alt="Robot Result">
      <div class="result-title" id="resultTitle"></div>
      <div class="result-score" id="resultScore"></div>
      <div class="result-msg" id="resultMsg"></div>
      <button class="close-btn" onclick="closeResult()">Close</button>
    </div>
  </div>
  <script>
    // PAGE LOGIC
    function showAssessment() {
      document.getElementById('welcomePage').style.display = 'none';
      document.getElementById('assessmentPage').style.display = '';
      startTimers();
      window.scrollTo(0,0);
    }

    // TIMER LOGIC
    let mcqTime = 10 * 60, totalTime = 30 * 60;
    let mcqTimer, totalTimer;
    function startTimers() {
      updateTimers();
      mcqTimer = setInterval(() => {
        if(mcqTime > 0) { mcqTime--; updateTimers(); }
      }, 1000);
      totalTimer = setInterval(() => {
        if(totalTime > 0) { totalTime--; updateTimers(); }
        if(totalTime === 0) { clearInterval(mcqTimer); clearInterval(totalTimer); submitAssessment(true);}
      }, 1000);
    }
    function updateTimers() {
      document.getElementById('mcq-timer').innerText = formatTime(mcqTime);
      document.getElementById('total-timer').innerText = formatTime(totalTime);
      // Auto-disable MCQs after 10 mins
      if(mcqTime === 0) {
        let mcqs = document.querySelectorAll('.mcq input[type=radio]');
        mcqs.forEach(el => el.disabled = true);
      }
    }
    function formatTime(sec) {
      let m = Math.floor(sec/60), s = sec%60;
      return (m<10?'0':'')+m+':'+(s<10?'0':'')+s;
    }

    // ASSESSMENT LOGIC
    document.getElementById('assessmentForm').addEventListener('submit', function(e){
      e.preventDefault();
      submitAssessment(false);
    });

    // Answers for MCQs. (lowercase)
    const mcqAnswers = ['b','c','c','c','c','b','c','c','c','b'];

    function submitAssessment(timeUp) {
      clearInterval(mcqTimer); clearInterval(totalTimer);
      // MCQ Scoring
      let scoreA = 0;
      for(let i=1; i<=10; i++) {
        let q = document.querySelector('input[name="q'+i+'"]:checked');
        if(q && q.value.toLowerCase() === mcqAnswers[i-1]) scoreA++;
      }
      let totalScore = scoreA; // out of 10
      // Section B: basic check for answer presence (2 marks each)
      let sectionB = 0;
      for(let i=1;i<=5;i++) {
        let ans = document.querySelector(`[name="b${i}"]`).value.trim();
        if(ans.length > 7) sectionB += 2;
      }
      totalScore += sectionB; // out of 20
      // Section C: check for descriptive answer
      let cAns = document.querySelector('[name="c1"]').value.trim();
      let secC = (cAns.length > 25) ? 5 : 0;
      totalScore += secC; // out of 25
      // Show result modal
      showResult(scoreA, sectionB, secC, totalScore, timeUp);
    }

    function showResult(a, b, c, total, timeUp) {
      let modal = document.getElementById('resultModal');
      let robotImg = document.getElementById('resultRobot');
      let title = document.getElementById('resultTitle');
      let score = document.getElementById('resultScore');
      let msg = document.getElementById('resultMsg');
      let percent = Math.round(total*100/25);
      score.innerText = `Your Score: ${a}/10 (MCQ) + ${b}/10 (Short) + ${c}/5 (Conceptual) = ${total}/25 (${percent}%)`;
      if(timeUp) {
        title.innerText = "Time's Up!";
        msg.innerText = "You ran out of time. Try to finish faster next attempt!";
        robotImg.src = "https://cdn.pixabay.com/photo/2017/01/31/13/14/robot-2027195_960_720.png";
      } else if(total >= 18) {
        title.innerText = "You nailed it!";
        msg.innerHTML = "<b>Fantastic job!</b> <br> The robot is happy. 🚀";
        robotImg.src = "https://cdn.pixabay.com/photo/2013/07/12/15/55/robot-150593_1280.png";
      } else {
        title.innerText = "Room for growth";
        msg.innerHTML = "Keep learning! The robot believes in you. 🤖✨";
        robotImg.src = "https://cdn.pixabay.com/photo/2017/01/31/13/14/robot-2027195_960_720.png";
      }
      modal.classList.add('show');
    }

    function closeResult() {
      document.getElementById('resultModal').classList.remove('show');
      window.scrollTo(0,0);
    }
  </script>
</body>
</html>
