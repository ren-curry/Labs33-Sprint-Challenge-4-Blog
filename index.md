# Data Scientist Ren Curry, A Study in SpaCy

## An introduction to the parties
Human Rights First (HRF) is an American advocacy and activist organization focused on human rights. The organization offers a pro bono legal representation program, which matches asylum seekers without the financial means to afford legal representation with attorneys who can advocate on their behalf. HRF seeks to expand its ability to aid asylum seekers by finding ways to utilize historical case data to better tailor their arguments when advocating for asylum seekers. For one month of my education with Lambda school I had the privilege of working with a cross discipline team of full stack web development students and data science students on the project for the HRF Asylum application. The project is to develop an application to process historical case data and provide the insights attorneys can utilize to improve their arguments for ongoing and future cases. My role was focused on the data science component of the application, which used optical character recognition (OCR) to read pdf case files and extract key information from the recognized text.

## A definition of problems
The HRF Asylum application is an ongoing project for Lambda School students, as such my team came into the application with an established codebase. The major goal for the data science component of the application was to improve the time and accuracy of the OCR scraping, text analysis, and key term retrieval. It was observed that the time the application was taking to complete the process of reading the images, To achieve one part of the overall goal, the team added the task of researching Python natural language processing (NLP) libraries for use in the text analysis. We came into the project using the spaCy library, so the task was to evaluate spaCy against other libraries to find which would be the most efficient for its use in the application.

## A plan is hatched
Diving into the task for researching NLP library options I came up with a plan. My task would initially begin with research, specifically researching the documentation for the top open source NLP libraries. The key libraries I chose were spaCy, Natural Language Toolkit (NLTK), and Bidirectional Encoder Representations from Transformers (BERT). I expected the research to take me between two and three days, depending the depth I might need to go into the documentation, for reading through the documentation and comparing the library options. After the research  about one day to review the current use of spaCy in the application in order to understand what switching would entail. After my research I would present to the team my decision.

## The adventure in solving
So the adventure of research in order to solve the problem began. To begin I reviewed spaCy documentation to further familiarize myself with the library. There I noticed a trend, most of the examples and benchmarks that spaCy claimed were state-of-the-art top performers. As an example the spaCy shows the following as the document processing Words Per Second:

![spaCy Speed Comparison](https://github.com/ren-curry/Labs33-Sprint-Challenge-4-Blog/blob/main/spacy_speed_comparison.png?raw=true)

At this point I decided to review our codebase and the measure of time I was using for evaluation. I realized that the time used was the total time from request from the back-end component to response to the back-end component. I needed to break apart the time values to identify the times for specific processes. Once I did so I found that the claims from spaCy were observable within our application, the spaCy text analysis process taking only a fraction of the total time with the bulk of the time being in the OCR processing.

Additionally while I was researching the spaCy, my teammates in the data science component were exploring use of the spaCy Matcher and PhraseMatcher packages. These packages worked seamlessly with the object created with the spaCy text analysis and had improved many of our methods for key term extraction.

## A solution provided
### Maintaining the use of spaCy as it is the state of the art choice and its many features worked well together. future challenge would be around the available trained NLP models with spaCy, no official "legal" model only one that has not recent maintenance

## Subtitle
### This one talk about how I have improved in labs, for me this will be more about talking about being a good move back into the workplace. explaining many of the lessons I had resonate well with how I have learned in the past working in my career. Then talk about how I liked working some where I "could make a difference" and solidifying my desire to move  strictly to back end data stuff. 
