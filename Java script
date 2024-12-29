// Quiz Functionality
const questions = [
  { question: "What is 2 + 2?", options: ["3", "4", "5"], answer: "4" },
  { question: "Capital of France?", options: ["Berlin", "Paris", "Madrid"], answer: "Paris" }
];

let currentIndex = 0;

const quizContainer = document.getElementById("quizContainer");
const questionElement = document.getElementById("question");
const optionsElement = document.getElementById("options");
const nextButton = document.getElementById("nextQuestion");

document.getElementById("startQuiz").onclick = () => {
  quizContainer.classList.remove("hidden");
  loadQuestion();
};

function loadQuestion() {
  const current = questions[currentIndex];
  questionElement.textContent = current.question;
  optionsElement.innerHTML = "";
  current.options.forEach(option => {
    const li = document.createElement("li");
    li.textContent = option;
    li.onclick = () => checkAnswer(option);
    optionsElement.appendChild(li);
  });
}

function checkAnswer(selected) {
  const correct = questions[currentIndex].answer;
  alert(selected === correct ? "Correct!" : "Wrong!");
  if (currentIndex < questions.length - 1) {
    currentIndex++;
    loadQuestion();
  } else {
    alert("Quiz Complete!");
    quizContainer.classList.add("hidden");
  }
}
