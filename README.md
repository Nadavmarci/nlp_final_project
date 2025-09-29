# Two-Agent Framework for Enhanced Performance on Multiple-Choice Question Answering

## Overview
This project was carried out as part of the NLP course in the M.Sc. program at Tel Aviv University.  
The work explores whether collaborative prompting with multiple Large Language Models (LLMs) can outperform single-model approaches on complex reasoning tasks.  

We introduce a **two-agent framework** for multiple-choice question answering (MCQA):
1. Two LLMs independently answer the same question and provide explanations for each choice.  
2. Their outputs are aggregated using one of two methods:
   - **Explanation-Based Answer Selection**: both models’ reasoning is compared across all choices.  
   - **Conflict Resolution**: if the models disagree, the framework compares only the conflicting answers with arguments and counter-arguments.  

The framework was evaluated on **OpenBookQA** and **AI2 ARC (Easy & Challenge)** datasets, using **Meta-Llama-3.2-3B-Instruct** and **Qwen2.5-3B-Instruct** models.

---

## Methods
- **Step 1**: Each model produces an answer and explanations for all choices.  
- **Step 2**: Aggregation of the answers using one of the two strategies above.  
- Baseline comparisons include:
  - Chain-of-Thought (CoT)
  - CoT + Self-Refine
  - CoT + Self-Consistency

---

## Results
- On OpenBookQA, both LLaMA and Qwen improved with aggregation methods.  
- On ARC datasets:
  - LLaMA consistently improved across all datasets.  
  - Qwen improved only on OpenBookQA but showed little or no change on ARC-Easy and ARC-Challenge.  
- Overall, the collaborative two-agent approach achieved performance close to or exceeding strong single-model baselines, with fewer inference iterations.  

Full results and analysis are presented in the report.

---

## Repository Structure
