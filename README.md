**AI Contract Clause Compliance Checker**


Objective:
Develop an AI system that evaluates whether a contract clause is compliant with a provided policy document using retrieval and semantic similarity.
Task Description:
Build a system that:
1.	Ingests a "Contract Rules & Compliance Document" (given to students)
2.	Converts clauses & rules into embeddings using sentence transformers
3.	For a given user clause: 
o	Retrieve similar sections from the rulebook
o	Evaluate compliance
4.	Generate: 
o	Compliance status
o	Reason for decision
o	Suggested corrected clause
o	Reference rules from the policy document
Input Example:
json
{
  "clause": "The vendor may share customer data with external partners without prior notice."
}
Expected Output:
json
{
  "compliance": "Not Compliant",
  "reason": "Unrestricted data sharing violates privacy and data governance rules.",
  "suggested_rewrite": "The vendor may share customer data only with approved third parties after obtaining explicit customer consent.",
  "matched_rule_reference": "Section 4.1 - Data Sharing Restrictions",
  "similarity_score": 0.89
}


Evaluation Criteria:
Criteria	Description	Weight
Retrieval Quality	Accuracy of rule matching	30%
Compliance Logic	Correct reasoning	30%
Rewrite Quality	Clarity, correctness & adherence	25%
Output Structure	Readable formatted response	15%
