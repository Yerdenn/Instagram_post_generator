# Instagram Content Generator
This script utilizes OpenAI's GPT-3.5-turbo model to generate engaging Instagram posts for real estate listings. It reads housing data from a CSV file, sends requests to the OpenAI API, and saves the generated content along with property details in a text file.

## Prerequisites
- Python 3.11.1
- An OpenAI API key
- A CSV file containing housing data (e.g., 'Housing.csv')
- A virtual environment is recommended for managing dependencies.

## Installation
1. Clone the repository:
```
git clone https://github.com/your-username/instagram-content-generator.git
cd instagram-content-generator
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Create a .env file in the project root and add your OpenAI API key:
```
TOKEN=your_openai_api_key_here
```

## Usage
1. Run the script:
```
python main.py
```
2. The script will sample 20 different property listings from the CSV file and generate alternative content for each. The results will be saved in a file named EXAMPLE.txt.

## Configuration
- Adjust the script parameters and OpenAI API settings in the script.py file as needed.
- Make sure the CSV file ('Housing.csv') follows the expected format with columns like 'price' and 'area'.

## Troubleshooting
- If you encounter issues, ensure the OpenAI API key is correctly set in the .env file.
- Verify that the CSV file is present and properly formatted.
## Disclaimer
This script is provided as-is, and users should review and comply with OpenAI's use case policies. The generated content may require manual review before publication.

## Questions:
1. How to mimic the style of *successful* Instagram posts?
2. What prompt engineering techniques can improve quality?
3. How to ensure the model doesn't invent extra features?
  
## Answers:

1. Mimicking the Style of Successful Instagram Posts:
To mimic the style of successful Instagram posts, you can provide specific instructions in your prompt to guide the language model. You may want to mention the desired tone, hashtags, or elements commonly found in successful posts. Experiment with different prompts until you achieve the desired style. Additionally, you can fine-tune the model using a dataset of successful Instagram captions to help it learn the specific patterns and styles.

2. Prompt Engineering Techniques for Quality Improvement:
- Clear Instructions: Provide clear and specific instructions in your prompt. Clearly state the information you want in the generated content.
- Temperature and Max Tokens: Adjust the temperature and max_tokens parameters. Higher temperature values (e.g., 0.8) make the output more diverse, while lower values (e.g., 0.2) make it more focused. Max_tokens limits the length of the output.
- System and User Messages: Utilize the system and user messages effectively. System messages set the behavior, and user messages provide the input. Experiment with the structure of the conversation to achieve the desired results.
- Iterative Refinement: If the initial output is not satisfactory, you can iteratively refine the prompt based on the model's responses.

3. Preventing the Model from Inventing Extra Features:

- Clear Instructions: Be explicit in your instructions about what information you want in the response. For example, specify that the model should only include features mentioned in the input data.
- Dataset Cleaning: Ensure that your input data is clean and doesn't contain ambiguous or conflicting information. This helps in preventing the model from inventing unrealistic details.
- Use of System Messages: Clearly define the context and constraints in the system message to guide the model's behavior. This can help in avoiding the introduction of unnecessary features.

Experimentation and fine-tuning based on the model's responses are crucial to achieving the desired results. Adjusting parameters and refining prompts will contribute to the quality and style of the generated content.
