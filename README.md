# Quiz-game-_Staxtech_project
# Simple Python Quiz Game

print("🎯 Welcome to the Python Quiz Game!")
print("Answer the questions by typing A, B, C, or D\n")

score = 0

# List of questions
questions = [
    {
        "question": "1. What is the capital of India?",
        "options": ["A. Mumbai", "B. New Delhi", "C. Chennai", "D. Kolkata"],
        "answer": "B"
    },
    {
        "question": "2. Which language is used for AI?",
        "options": ["A. Python", "B. HTML", "C. CSS", "D. SQL"],
        "answer": "A"
    },
    {
        "question": "3. Who developed Python?",
        "options": ["A. Elon Musk", "B. Mark Zuckerberg", "C. Guido van Rossum", "D. Sundar Pichai"],
        "answer": "C"
    }
]

# Quiz loop
for q in questions:
    print(q["question"])
    for option in q["options"]:
        print(option)

    user_answer = input("Your answer: ").upper()

    if user_answer == q["answer"]:
        print("✔ Correct!\n")
        score += 1
    else:
        print("❌ Wrong! Correct answer is:", q["answer"], "\n")

# Final score
print("🎉 Quiz Completed!")
print(f"Your final score: {score}/{len(questions)}")

if score == len(questions):
    print("🔥 Excellent! You got all correct!")
elif score >= 1:
    print("👍 Good job! Keep practicing.")
else:
    print("😢 Better luck next time!")
