-- Active: 1735111327105@@127.0.0.1@3306@quizappdesignv1
INSERT INTO Users (name, role) 
VALUES
('Alice Johnson', 'student'),
('Bob Smith', 'teacher'),
('Catherine Lee', 'student'),
('Daniel Brown', 'teacher'),
('Emily Davis', 'student');


INSERT INTO quizzes (title, description, teacher_id)
VALUES
('Math Basics', 'An introductory quiz covering basic math concepts.', 2),
('Science Fundamentals', 'A quiz to test knowledge of fundamental science principles.', 4),
('History 101', 'Questions about significant historical events and dates.', 2),
('Programming Essentials', 'Covers basic concepts in programming.', 4),
('Geography Quiz', 'Focuses on world geography and map reading skills.', 2);


INSERT INTO questions (question, quiz_id)
VALUES
('What is 2 + 2?', 1),
('Name the process by which plants make their food.', 2),
('Who was the first president of the United States?', 3),
('What is the output of 2 * 3 in Python?', 4),
('What is the capital of France?', 5);


-- Options for Question 1: "What is 2 + 2?"
INSERT INTO options (question_id, option_text, is_correct)
VALUES
(1, '3', FALSE),
(1, '4', TRUE),
(1, '5', FALSE),
(1, '6', FALSE);

-- Options for Question 2: "Name the process by which plants make their food."
INSERT INTO options (question_id, option_text, is_correct)
VALUES
(2, 'Respiration', FALSE),
(2, 'Photosynthesis', TRUE),
(2, 'Transpiration', FALSE),
(2, 'Digestion', FALSE);

-- Options for Question 3: "Who was the first president of the United States?"
INSERT INTO options (question_id, option_text, is_correct)
VALUES
(3, 'George Washington', TRUE),
(3, 'Abraham Lincoln', FALSE),
(3, 'Thomas Jefferson', FALSE),
(3, 'John Adams', FALSE);

-- Options for Question 4: "What is the output of 2 * 3 in Python?"
INSERT INTO options (question_id, option_text, is_correct)
VALUES
(4, '5', FALSE),
(4, '6', TRUE),
(4, '8', FALSE),
(4, '3', FALSE);

-- Options for Question 5: "What is the capital of France?"
INSERT INTO options (question_id, option_text, is_correct)
VALUES
(5, 'Paris', TRUE),
(5, 'London', FALSE),
(5, 'Berlin', FALSE),
(5, 'Madrid', FALSE);


INSERT INTO Student_answers (student_id, quiz_id, question_id, option_id)
VALUES
-- Student 1 answers Question 1 in Quiz 1
(1, 1, 1, 2), -- Student selects correct option for "What is 2 + 2?"

-- Student 1 answers Question 2 in Quiz 2
(1, 2, 2, 6), -- Student selects correct option for "Name the process by which plants make their food."

-- Student 2 answers Question 3 in Quiz 3
(2, 3, 3, 9), -- Student selects correct option for "Who was the first president of the United States?"

-- Student 2 answers Question 4 in Quiz 4
(2, 4, 4, 11), -- Student selects correct option for "What is the output of 2 * 3 in Python?"

-- Student 1 answers Question 5 in Quiz 5
(1, 5, 5, 13); -- Student selects correct option for "What is the capital of France?"

