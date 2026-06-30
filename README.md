# rkca-resettlement-assistant
AI decision support system for refugee resettlement casework 

RKCA: ResettleAid Knowledge and Case Assistant
RKCA_TestRunner_Final-2.html is a self-contained browser application. It holds the knowledge base, all prompts, and the evaluation harness in a single file, with no installation or server required.
The three-layer architecture
RKCA routes each caseworker query through a master system prompt to one of three function layers:
1.	Policy Navigation: retrieves and explains the relevant Standard Operating Procedure (SOP), surfacing prerequisites and dependencies.
2.	Case Prioritization: ranks a family's pending actions by deadline proximity and consequence severity, using Chain-of-Thought reasoning.
3.	Workflow Coordination: maps the dependency chain between tasks, identifies what is blocked and by what, and produces a sequenced action plan.



All three are grounded in a nine-document knowledge base (six SOPs, two referral directories, and a deadline calendar) embedded directly in the application.

How to run the Test Runner


The Test Runner is a single HTML file with no installation or server required.
1.	Download RKCA_TestRunner_Final-2.html from this repository.
2.	Open it in any modern web browser (Chrome, Edge, Firefox, or Safari).
3.	To run live evaluations, paste a Google AI Studio (Gemini) API key into the configuration panel. The key is entered at runtime and is not stored or shared.
4.	Under the “Prompt Version” start by selecting Version 1, and pick one of the eight built-in test cases (TC-01 to TC-08) under the “Test Cases” section. Or you can also enter your own test query.
5.	Click “Run Test” to send the query to Gemini and view the grounded response, the “Score Response” section is what was used to score the response and save logs that were presented as the table in the main paper
6.	You can repeat the exact same steps to run the test against Version 2 of the model. 
7.	The Function section serves to show which of the function layer is being tested by the case study, so it will highlight after the response from the AI
Even without the API Key it is possible to inspect the full system without running it: the embedded knowledge base, the verbatim V1 and V2 prompts, and all eight test-case profiles are visible in the interface and in the file's source. The "Prompt Preview" pane shows the exact text sent to the model.


