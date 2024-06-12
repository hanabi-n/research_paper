# Using the SVC and LLM models to detect the SQL Injection vulnerability in code

Injection attacks are a major concern ranking third in dangerous cybersecurity attacks [[1](https://owasp.org/Top10/A03_2021-Injection/)]. SQL Injection is one of the types responsible for 23 per cent of security vulnerabilities worldwide [[2](https://www.statista.com/statistics/806081/worldwide-application-vulnerability-taxonomy/)]. In this research, we find an effective way to detect SQL Injection vulnerability in code using the Support Vector Classifier machine learning model and Large Language Model approaches. 

### Methods
We obtained three datasets ([[3](https://dl.acm.org/doi/10.1145/3607199.3607242)] [[4](https://dl.acm.org/doi/10.1145/3576915.3623175)][[5](https://arxiv.org/abs/2311.12420)]) with 514 values. To compare the SVC and LLM models, we used two different approaches: 
<ol>
  <li> The numerical feature vectors to process the SVC model’s dataset</li>
  <li> Converting the dataset into an acceptable format for the website OpenAI to work with the LLM.</li>
</ol>

<p style="text-align: center;">Methodology figure</p>

<img 
    style="display: block; 
           margin-left: auto;
           margin-right: auto;
           width: 60%;"
    src="https://github.com/hanabi-n/research_paper/assets/53466808/d3a965e6-d77e-4101-b034-2e70ca651ce0" 
    alt="Our logo">
</img>

<p style="text-align: center;">Dataset distribution</p>

<img 
    style="display: block; 
           margin-left: auto;
           margin-right: auto;
           width: 60%;"
    src="https://github.com/hanabi-n/research_paper/assets/53466808/a8b68db6-a461-4d46-8a71-2dfd8e00f831" 
    alt="Our logo">
</img>

### Results
After comparing the SVC and Large Language models, the fine-tuning model achieved promising results in detecting SQL Injection vulnerabilities. The fine-tuning model based on gpt-3.5- turbo-1106 showed a high accuracy metric of 98 per cent.

| Models | True positive | False positive | True negative | False negative | Accuracy | Precision | Recall | F1 score |
|--------|---------------|----------------|---------------|----------------|----------|-----------|--------|----------|
| SVC    | 69            | 2              | 80            | 4              | 0.9613   | 0.9718    | 0.9452 | 0.9583   |
| LLM    | 70            | 0              | 82            | 3              | 0.9806   | 1.0       | 0.9589 | 0.979    |

### Future work
Future work aims to use an abstract syntax tree (AST) tool and the recent LLM models to reach higher performance. The findings from the research have the potential to automate vulnerability detection within the development pipeline.
