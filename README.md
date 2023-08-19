# Baseball Free Response Question Generator and Evaluation

This project aims to simulate the process of generating free response questions (FRQs) related to baseball using OpenAI's GPT-3 language model, as well as evaluating and providing feedback on student responses to these questions. The project consists of several scripts that work together to achieve this goal.

## Files and Usage

1. **freeResponseGen.py**: This script generates new prompts for free response questions about baseball using the GPT-3 language model. It evaluates the quality of the prompts using predefined criteria and appends suitable prompts to the existing list of prompts in "prompts.txt". To use this script:

   - Set your OpenAI API key in the `openai.api_key` variable.
   - Run the script using `python freeResponseGen.py`.

2. **genResponse.py**: This script generates student responses to the FRQs based on the existing prompts. It assigns personas to the student responses, generates responses using GPT-3, and saves the responses along with personas and prompts to "responses.txt". To use this script:

   - Set your OpenAI API key in the `openai.api_key` variable.
   - Run the script using `python genResponse.py`. Run this script after running `freeResponseGen.py`.

3. **promptEval.py**: This module contains a function `evaluate_prompt_quality(prompt)` that evaluates the quality of a prompt based on specific keywords. This function is used in the `freeResponseGen.py` script to filter and select suitable prompts.

4. **responses.txt**: This file contains generated student responses to the FRQs. Each response is associated with a persona, prompt, and personality trait.

5. **prompts.txt**: This file contains a list of existing prompts for FRQs related to baseball. New prompts generated by the `freeResponseGen.py` script are appended to this list.

6. **grader.py**: This script simulates the process of evaluating student responses to the FRQs. It uses predefined personas and Common Core standards to evaluate the responses and provides feedback.

7. **studentFeedback.txt**: This file contains the feedback provided by the teacher for each student response. It includes the original FRQ, the student's response, and the teacher's feedback.

8. **conversation.py**: This script simulates a conversation between a student and a teacher. It takes a student response from `studentFeedback.txt`, generates a teacher response using the `provide_teacher_response` function from `grader.py`, and outputs the conversation to `transcript.txt`.

9. **transcript.txt**: This file contains the simulated conversation between the student and teacher, including the original FRQ, student response, teacher feedback, and teacher response.

## Usage Instructions

1. Run `freeResponseGen.py` to generate new prompts for FRQs related to baseball and evaluate their quality.

2. Run `genResponse.py` to generate student responses based on the existing prompts.

3. Use `grader.py` to simulate the evaluation of student responses based on personas and Common Core standards.

4. Run `conversation.py` to simulate a conversation between a student and a teacher, incorporating student responses, teacher feedback, and teacher responses.

## Important Note

- Ensure that you set your OpenAI API key in the appropriate scripts.
- The provided scripts and functions are illustrative examples and can be customized to better suit your project's requirements.
