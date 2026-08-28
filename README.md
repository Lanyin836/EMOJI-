# EMOJI-# README: Data Availability, De-identification, and Reproducibility

This folder contains de-identified derived datasets, coding files, statistical outputs, and analysis scripts associated with the manuscript:

**When Emojis Mislead Sentiment Analysis: Pragmatic Drift, Semantic Asymmetry, and Emoji Polarity in Chinese Digital Discourse**

The files are provided to support analytical reproducibility while protecting questionnaire participants and reducing risks associated with user-generated social media content.

## Data Collection Period

The questionnaire data were collected between October 11, 2025 and November 14, 2025.

## Included Materials

### Corpus-Derived FPEI Data

- `deidentified_emoji_count_matrix_for_FPEI.xlsx`

This file is the main public reproducibility dataset for the False-Positive Emoji Index (FPEI) analysis. It does not contain raw comment text. Each row represents one anonymized analytical record and includes only:

- anonymous comment ID;
- corpus type (`false_positive`, `model_positive`, or `model_negative`);
- occurrence counts for the 20 emojis reported in Table 1.

This matrix can be used to reproduce `fp_per_1000`, `pos_per_1000`, `neg_per_1000`, FPEI values, bootstrap confidence intervals, and comment-level sensitivity analyses.

### Statistical Output Files

- `emoji_FPEI_bootstrap_CI_and_sensitivity.xlsx`
- `emoji_FPEI_from_deidentified_matrix_check.xlsx`
- `annotation_reliability_sensitivity_analysis.xlsx`
- `emoji_questionnaire_blind_consistency_analysis.xlsx`
- `emoji_semantic_polarity_scores_20_items_by_filename.xlsx`

These files report the statistical results used in the revised manuscript, including FPEI estimates, bootstrap confidence intervals, inter-annotator reliability, questionnaire coding consistency, polarity scores, quadrant positions, and chi-square tests.

### Questionnaire Coding Files

- `types-annotator 1/`
- `types-annotator 2/`
- `五类语义编码规则.docx`

The `types-annotator 1` folder contains the first-round five-category semantic coding for the 20 emoji questionnaire items. The `types-annotator 2` folder contains blind review samples coded by a second annotator for reliability checking. The coding rule document describes the five semantic categories used in the questionnaire analysis.

### Analysis Scripts

- `analysis_scripts/`

The scripts reproduce the main reported analyses from the submitted derived datasets. See `analysis_scripts/README_analysis_scripts.md` for details.

For public reproducibility of the FPEI analysis, the preferred script is:

- `analysis_scripts/06_FPEI_from_deidentified_matrix.py`

This script reads only `deidentified_emoji_count_matrix_for_FPEI.xlsx` and does not require raw comment text.

## Materials Not Publicly Redistributed

The raw social media comment corpus is not publicly redistributed because it consists of user-generated social media content that may contain identifiable or traceable textual information and may be subject to platform terms-of-service and copyright restrictions.

The raw corpus files used during analysis included comments classified by the sentiment analysis API as positive, negative, or neutral, as well as the manually validated false-positive corpus. For public sharing, these raw text files have been replaced by the de-identified emoji count matrix described above.

Item-level offensiveness ratings linked to the restricted raw comment corpus are not fully redistributed in text-linked form. To support transparency, the aggregated reliability results are provided in `annotation_reliability_sensitivity_analysis.xlsx`, and the script used to calculate Fleiss' kappa, Krippendorff's alpha, ICC, and sensitivity checks is provided in `analysis_scripts/02_annotation_reliability.py`. De-identified item-level rating files can be made available upon reasonable request where permitted by institutional and platform-related data restrictions.

## Privacy and De-identification

Before public sharing, the datasets were processed to remove or avoid information that could directly or indirectly identify questionnaire participants or social media users.

The public corpus-derived files do not include:

- raw social media comment texts;
- usernames;
- social media profile information;
- links;
- timestamps;
- original row numbers from the raw corpus;
- account identifiers or other identifying metadata.

The public questionnaire-related files do not include:

- participant names;
- phone numbers;
- email addresses;
- IP addresses;
- precise questionnaire submission timestamps;
- original questionnaire platform sequence numbers.

Where participant-level or response-level data are included, records are organized for analysis using non-identifying item labels or anonymized analytical structure.

## Reproducibility Notes

The Baidu Sentiment Analysis API screening step is not reproduced here because the API is a commercial closed-source system and may produce version-dependent results. The submitted scripts begin from saved model-classified and manually annotated derived datasets used in the revised analysis.

The de-identified matrix and statistical output files are intended to reproduce the analyses reported in the manuscript, rather than to redistribute the original social media corpus.


## Terms and Reuse

The shared files are intended for verification of the analyses reported in the manuscript and for non-commercial academic research. Users should not attempt to re-identify questionnaire participants, social media users, or the original comment source from the shared materials.
