# PSLE Math Analysis

How to use:
* Eval-results-and-error-analysis:
    * raw_mmd.md is OCR MD output of PSLE paper from [MathPix](https://mathpix.com/) API
        * uses LaTeX for representing math formulas
    * To get raw_mmd.md -> questions.jsonl, use parse-md.ipynb
    * use run-p1a-ans.ipynb to generate ai-answers.md, then manually check with answer key and manually compose error-analysis.md
        * ai-answers.md has some minor manual touch ups but shouldn't be too far from raw output
        * i.e. I manually add the Answer Key Answer currently
* parse-md.ipynb
    * question format optimised for use of Structured Input into model, sometimes multiple images can be sent, no images ok.
* run-p1a/p1b-eval.ipnb
    * have different code to handle different question and answer formats for MCQ (p1-bookA) and SAQ (p1-bookB)

To Improve:
* MathPix API is convenient and powerful for OCR but expensive for scale
    * i.e. 2B llama tokens requires ~ 3.3M pages of OCR, which will cost ~$80K with current pricing
    * looking into self-hosting [Marker](https://github.com/VikParuchuri/marker)