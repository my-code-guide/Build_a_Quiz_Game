const question1 = {
  category: "Animals",
  question: "Why can't a penguin fly?",
  choices: [
    "A. It forgot how", 
    "B. It has no wings", 
    "C. Its wings are adapted for swimming"
    ],
  answer: "C. Its wings are adapted for swimming"
}

const question2 = {
  category: "Food",
  question: "What happens if you put a banana in your pocket for three days?",
    choices: [
      "A. It becomes a phone", 
      "B. It becomes banana soup", 
      "C. It gets very happy"
      ],
    answer: "B. It becomes banana soup"
}

const question3 = {
  category: "Space",
  question: "What would happen if you tried to scream on the Moon?",
    choices: [
      "A. Aliens would hear you", 
      "B. Nobody would hear you", 
      "C. The Moon would scream back"
      ],
    answer: "B. Nobody would hear you"
}

const question4 = {
  category: "Everyday Life",
  question: "Why does the TV remote always disappear when you need it?",
    choices: [
      "A. The couch eats it", 
      "B. It is training for hide-and-seek", 
      "C. All of the above"],
    answer: "C. All of the above"
}

const question5 = {
  category: "Animals",
  question: "What is a group of flamingos called?",
  choices: [
    "A. A pink army", 
    "B. A flamboyance", 
    "C. A squad"
    ],
  answer: "B. A flamboyance"
}

const questions = [question1, question2, question3, question4, question5]

const getRandomIndex = (array) => Math.floor(Math.random() * array.length)

const getRandomQuestion = (questions) => questions[getRandomIndex(questions)]

const getRandomComputerChoice = (choices) => choices[getRandomIndex(choices)]

const getResults = (question, choice) => {
  return choice === question.answer ? "The computer's choice is correct!" : `The computer's choice is wrong. The correct answer is: ${question.answer}`
}

console.log(getRandomQuestion(questions))

