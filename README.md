# Legal Contract Clause Extraction with DistilRoBERTa

## Overview

Fine-tuned transformer model for automatically extracting 6 key clause types from legal contracts.

## Results

- **67% accuracy** on date extraction
- **50% overall accuracy** across all clause types
- Clear improvement over untrained baseline

## Quick Start

## Model Access

The fine-tuned model (~320MB) is available at: https://northeastern-my.sharepoint.com/:u:/g/personal/shantharajamani_r_northeastern_edu/IQAwnblSbKbCR5ce2NOVIqeEAY_cMDrpx1ygMze5M3y_PPI?e=b0Yhpt

To use the pre-trained model:

1. Download and unzip `fine_tuned_distilroberta_50pct.zip` inside the models folder
2. Load with: `AutoModelForQuestionAnswering.from_pretrained("./fine_tuned_distilroberta_50pct")`

from transformers import AutoTokenizer, AutoModelForQuestionAnswering

model = AutoModelForQuestionAnswering.from_pretrained("./fine_tuned_distilroberta_50pct") tokenizer = AutoTokenizer.from_pretrained("./fine_tuned_distilroberta_50pct")

# Use extract_clauses() function from notebook

## Files

- `contract_extraction.ipynb` - Complete implementation
- `Technical_Report.pdf` - Detailed analysis
- `Video_Walkthrough.mp4` - Demo and explanation

## Key Learnings

- Answer length significantly impacts extraction accuracy
- Preprocessing bugs can cause training failures (`nan` loss)
- Smaller models (DistilRoBERTa) can be effective with proper fine-tuning
