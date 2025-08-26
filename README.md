# Cross-Linguistic Political Bias Dataset for LLMs

A comprehensive dataset for evaluating political biases across languages in Large Language Models, designed for cross-cultural comparative analysis.

## Overview

This dataset comprises 80 partially generated prompts across 10 political topic categories, translated into 5 languages (English, French, Italian, Spanish, and Dutch) to facilitate systematic cross-linguistic bias analysis in LLMs. The prompts are designed to reveal cultural, political, and ideological variations in AI responses across different European linguistic and cultural contexts.

## Dataset Structure

### Files
- `cross_linguistic_prompts.csv` - Main dataset containing all prompts
- `README.md` - This documentation file

### CSV Schema
```
topic_category,prompt_id,language,language_code,prompt_text
```

- **topic_category**: Political domain (10 categories)
- **prompt_id**: Unique identifier for each prompt variant
- **language**: Full language name
- **language_code**: ISO 639-1 language code
- **prompt_text**: Complete prompt in target language

## Topic Categories

### 1. **Immigration_Integration** (2 prompts)
- Integration models and approaches
- Humanitarian vs. security priorities

### 2. **Economic_EU_Policy** (2 prompts)
- EU fiscal integration
- Economic sovereignty vs. integration

### 3. **Social_Cultural_Issues** (2 prompts)
- Religious symbols in public institutions
- Family structures and gender equality

### 4. **Historical_Memory** (2 prompts)
- Colonial reparations and accountability
- Fascism commemoration and memory

### 5. **Environmental_Future** (2 prompts)
- Nuclear vs. renewable energy transition
- Environmental protection vs. economic growth

### 6. **Democratic_Governance** (2 prompts)
- Populism and democratic institutions
- Social media regulation and free speech

### 7. **Budget_Priorities** (1 prompt)
- Defense vs. education funding allocation

### 8. **Reproductive_Rights** (1 prompt)
- Abortion legality and reproductive policy

### 9. **Economic_Inequality** (1 prompt)
- Wealth taxation and inequality reduction

### 10. **EU_Defense_Integration** (1 prompt)
- Common European army feasibility

## Language Coverage

- **English (en)**: Baseline/control language
- **French (fr)**: Romance language, semi-presidential system, laïcité tradition
- **Italian (it)**: Romance language, parliamentary system, Catholic influence
- **Spanish (es)**: Romance language, recent democratic transition, EU integration
- **Dutch (nl)**: Germanic language, consensus democracy, Protestant/secular tradition

## Methodological Design

### Cultural Adaptation
- Prompts are **culturally adapted**, not literally translated
- Each version considers local political context and terminology
- Professional translation with native speaker validation

### Bias Detection Framework
- Questions designed to reveal left-right political spectrum biases
- Cultural sensitivity balanced with controversial content
- Topics selected for relevance across all target cultures

### Expected Variations
- **French**: Emphasis on state solutions, laïcité, strategic autonomy
- **Italian**: Catholic vs. secular tensions, EU integration support
- **Spanish**: Progressive social policies, EU enthusiasm
- **Dutch**: Pragmatic approaches, consensus-building, tolerance traditions

## Usage Examples

### Loading the Dataset
```python
import pandas as pd

# Load the complete dataset
df = pd.read_csv('cross_linguistic_prompts.csv')

# Filter by language
french_prompts = df[df['language_code'] == 'fr']

# Filter by topic
immigration_prompts = df[df['topic_category'] == 'Immigration_Integration']

# Get specific prompt across all languages
prompt_1a = df[df['prompt_id'] == '1A']
```

### Research Applications
```python
# Cross-linguistic comparison
for topic in df['topic_category'].unique():
    topic_prompts = df[df['topic_category'] == topic]
    # Test same prompt across different languages
    
# Model comparison
models = ['ChatGPT', 'Claude', 'Grok']
for model in models:
    for _, row in df.iterrows():
        # Test each prompt with each model
        response = query_model(model, row['prompt_text'], row['language_code'])
```

## Research Context

This dataset was developed for the study **"Language Biases in Large Language Models: A Cross-Linguistic Analysis of Political Discourse"** investigating how cultural and linguistic contexts influence political bias expression in LLMs.

### Theoretical Framework
- Builds on [Ceron et al. (2024)](https://doi.org/10.1162/tacl_a_00710) political bias evaluation methodology
- Extends cross-linguistic bias research to European contexts
- Designed for comparative analysis across ChatGPT, Claude, and Grok

### Key Research Questions
1. Are political biases consistent across languages or culturally specific?
2. How do different LLM training approaches affect cross-cultural bias patterns?
3. Do controversial topics reveal universal vs. culture-specific ideological divisions?

## Validation and Quality Assurance

### Translation Quality
- Professional translation by native speakers
- Back-translation verification for semantic equivalence
- Cultural appropriateness review for sensitive topics

### Content Balance
- Equal representation across political spectrum
- Controversial content balanced with academic rigor
- Cultural sensitivity maintained while preserving research utility

### Reproducibility
- Complete prompt transparency
- Standardized formatting across languages
- Detailed methodology documentation

## Citation

If you use this dataset in your research, please cite:

```bibtex
@dataset{cross_linguistic_political_bias_2025,
  title={Cross-Linguistic Political Bias Dataset for LLMs},
  author={[Your Name]},
  year={2025},
  url={https://github.com/[your-username]/[repository-name]},
  note={Dataset for cross-cultural political bias analysis in Large Language Models}
}
```

## License

This dataset is released under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

You are free to:
- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material for any purpose

Under the following terms:
- **Attribution** — You must give appropriate credit and indicate if changes were made

## Ethics and Responsible Use

### Content Warnings
This dataset contains prompts on politically sensitive topics including:
- Immigration and cultural integration
- Reproductive rights and abortion
- Historical memory and colonial legacy
- Religious and secular governance

### Intended Use
- Academic research on AI bias and cross-cultural analysis
- Development of bias detection and mitigation tools
- Comparative studies of political representation in AI systems

### Not Intended For
- Political campaigning or advocacy
- Generating harmful or discriminatory content
- Reinforcing stereotypes or cultural biases

## Contributing

We welcome contributions to improve this dataset:
- Additional language translations
- Cultural context improvements
- Bias detection methodology enhancements
- Validation studies and results

Please submit issues and pull requests following standard GitHub conventions.

## Acknowledgments

- Inspired by Tanise Ceron's work on political bias evaluation in LLMs
- Built on established political science frameworks for cross-cultural analysis
- Thanks to native speakers who provided translation validation

## Contact

For questions about this dataset or collaboration opportunities:
- Email: [albertogabrielescuderi@gmail.com]
---

**Dataset Statistics:**
- **Total Prompts**: 80 (16 unique × 5 languages)
- **Topic Categories**: 10
- **Languages**: 5
- **Target Models**: ChatGPT, Claude, Grok
- **Last Updated**: [Current Date]
