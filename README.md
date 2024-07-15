Problem Statement


PS-17 Business Contract Validation:
To classify content within the Contract Clauses & to determine deviations from Template & highlight them






Unique Idea Brief (Solution)


●	Our Idea was to use unique, and advanced LLM agents powered by LangChain and GroqCloud API for fast results, through which we use LLama 3 to power our agents.
●	It must be noted that (if required) we can run our application locally using OLLama as well, to serve the LLMs for our agents. 
●	These smart LLM agents allowed us to read a contract and classify it, get the key entities out of it and identify and highlight the deviations in it. 
●	These agents were designed and executed in flow using ‘Crew AI’, a smart LLM handling software that allows for easy creation and control of LLM processes.

●	We used the PyMuPDF PDF loader to get the content out of the contract PDF and kickoff the crew of agents and processes to classify, compare, find deviations and highlight them in the contract text.

●	The project also contains a slick and fast Flask backbone and a minimalistic React Frontend to create the final application for contract analysis






Features Offered

●	Vast array of LLM agents to tackle the entire contract analysis process.
●	Access to LLama 3 for powering our agents with speed, efficiency, accuracy, fluency and adaptability.
●	Powered by LangChain and GroqCloud for lightning-fast API access
●	Hand-crafted LLM agents for : 
a.	classifying the contracts
b.	Identifying the key entities 
c.	Comparing the contract to a template to discover 
d.	Highlight the deviations with clear explanations as to how they deviate
●	Flask API backbone to connect frontend windows with backend agents to serve the application functions to the user
●	React Frontend to present the required contract analysis results 
Process Flow

1.	The application receives the contract PDF to be analysed (In the frontend window)
2.	The contract PDF is then loaded and parsed using PyMuPDF to extract the content of the contract for further downstream analysis
3.	The contract is first classified into one of a few select basic and common contract types based on the content of the contract, using a ‘categorizer_agent’ and ‘categorize_contract’ task. This task, along with this agent, is executed as one crew to obtain the contract type, which will prove to be important context for future processes
4.	Then, using the contract type we just found out, we will take a Key Entities template for that contract type, and then use a ‘contract_KeyEntity_Recognizer’ agent and task to extract key entities and a re-verifier agent to review and check the first agent’s performance to provide a more accurate list of key entities that are present and key entities that are absent.
5.	 After this, we then use the contract type found earlier to take a contract template for that type, which we will then use to compare with the contract PDF provided to identify and pinpoint the deviations in the given contract PDF, as well as provide an explanation as to why that deviation was deemed as such. This is done via a “contract_deviation_agent” and the “contract_Deviation_Identifier” task.
6.	Finally, the output of the above agent and task is fed as context to a highlighting agent, whose job it is to highlight the lines, clauses and sub-clauses where the deviation has been identified, highlight them in the extracted text of the contract PDF and provide an ‘i’ button that when clicked will provide the explanation for the deviation tag being levied on the highlighted text.
Architecture Diagram

Technologies used


●	PyMuPDF
●	LLama 3
●	GroqCloud
●	CrewAI
●	LangChain
●	Zoho Contracts (for contract templates)
●	Flask
●	React



Team members and contribution:


●	Karthik Sabareesh:
a.	Designing the LLM Agents
b.	 App testing, and debugging
c.	Deviation Identification flow design

●	Vishveshwara:
a.	Designing the LLM Agents
b.	 App testing, and debugging
c.	React frontend design
d.	Key Identities flow design


Conclusion


In conclusion, We have designed a novel solution that takes advantage of the ever-growing capabilities of large LLMs like LLama 3, and advanced frameworks like Crew AI, GroqCloud and LangChain to create LLM powered Agents that can read, classify and analyze contracts to extract key entities and identify deviations. We have designed an application that provides a fast, stable and efficient solution that can reliably provide the required solution to the given problem statement and perform to a high degree of efficiency, accuracy and adaptability. This project reflects weeks of research, design, debugging and hard work from our team. I would like to thank INTEL, our faculty mentors, Mr. Nandy, and VIT Chennai for providing us with the opportunity and guidance required to help us create and achieve what we have, as a part of the INTEL Unnati Industrial Internship.


Thank You

By:
Karthik Sabareesh
Vishveshwara
(Team PandaLake)
