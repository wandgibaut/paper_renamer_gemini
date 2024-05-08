# Paper Renamer Gemini

Paper Renamer is a script that automatically renames PDF files based on their content. Using Google's Gemini, the script extracts the first author's surname, the year of publication, and title to generate a meaningful filename. The advantage of this approach is that it can handle arbitrarily formatted pdfs. 

### Examples
[[Zhao 2023] LLaMA_Beyond_English_An_Empirical_Study_on_Language_Capability_Transfer.pdf](https://arxiv.org/abs/2401.01055)

[[Hong 2022] CogAgent_A_Visual_Language_Model_for_GUI_Agents.pdf](https://arxiv.org/abs/2312.08914)

[[Gromov 2022] The_Unreasonable_Ineffectiveness_of_the_Deeper_Layers.pdf](https://arxiv.org/abs/2403.17887)
## Installation
Download repo:
```
git clone https://github.com/wandgibaut/paper_renamer_gemini/
```
Install relevant python modules:
```
pip install -r requirements.txt
```
## Usage
set GOOGLE_API_KEY with your google api key in the environment variables.

Pass the directory containing the script as argument and run:

```
python paper_renamer.py --dir /path/to/pdfs
```

The script will process PDFs in the current directory and rename them. It will also create and update a json file with papers already processed to ensure the same info isn't sent multiple times. 

## Notes
This repo is based on the work of [ksmith9](https://github.com/ksmith9/paper_renamer_gpt), from which I've made a [fork](https://github.com/wandgibaut/paper_renamer_gpt) and adapted the code to use Google's Gemini instead of OpenAI's GPT-4.

### License

[MIT License](https://choosealicense.com/licenses/mit/)
