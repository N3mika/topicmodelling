# Modeling Topics and Sociolinguistic Variation in Code-Switched Discourse: Insights from Spanish-English and Spanish-Guaraní  
Nemika Tyagi*, Nelvin Licona-Guevara, Olga Kellert  
Arizona State University - ntyagi8@asu.edu  

---

## Overview

This repository contains the bilingual corpora and annotated resources described in the paper:

> **Tyagi, N., Licona-Guevara, N., & Kellert, O. (2026).**
> *Modeling Topics and Sociolinguistic Variation in Code-Switched Discourse: Insights from Spanish-English and Spanish-Guaraní.*

The datasets were enriched using an LLM-assisted annotation pipeline for topic and sociolinguistic labeling.  
Each dataset includes topic, discourse/pragmatic, or formality-level annotations that support large-scale, interpretable analysis of bilingual communication.

---

## 1️. Miami Bilingual Corpus Subset (`miami_sent.xlsx`)

**Source:** [Bangor Miami Corpus of Spanish–English Bilingual Speech (Deuchar et al., 2014)](https://bangortalk.org.uk)

**Description:**  
A subset of 2,825 intra-sententially code-switched sentences, annotated for:
- **Topics:** Domain/content category (e.g., *Casual_EverydayTalk*, *Narratives_Quotations*, *Workplace_Technical*).
- **Functions:** Discourse or pragmatic role (e.g., *Narrative*, *PrecisionLexicalGap*, *Directive*).
- **Sociolinguistic metadata:** Speaker age, gender, relation, and conversational situation.

**Columns:**
| Field | Description |
|-------|-------------|
| `sent_id` | Sentence identifier from original corpus |
| `filename` | Source transcript name |
| `sentence` | Transcribed bilingual sentence |
| `tokens_info` | List of token-level language tags (`token`, `lang_tag`) |
| `sen_len` | Sentence length in tokens |
| `speaker` | Speaker ID (anonymized) |
| `age`, `gender` | Speaker demographic info |
| `situation`, `relation` | Interactional metadata |
| `topic`, `function`, `secondary_function` | GPT-based topic/function annotations |
| `count_english`, `count_spanish` | Token counts by language |

---

## 2️. Spanish–Guaraní Dataset (`spa_gua_sent.xlsx`)

**Source:** [GUA-SPA: Guaraní–Spanish Code-Switching Corpus (Chiruzzo et al., 2023)](http://journal.sepln.org/sepln/ojs/ojs/index.php/pln/article/view/6563)

**Description:**  
A subset of 866 code-switched sentences from Paraguayan tweets and news articles.  
Each sentence is annotated for register and topical dimensions:
- **Formality:** *Formal* (institutional, objective) or *Informal* (personal, conversational).  
- **Genre:** e.g., *News*, *Personal*, *Politics*, *Education*.  
- **Topic:** e.g., *Government_Announcement*, *Personal_Emotional*, *Corruption_Donations_Procurement*.  

**Columns:**
| Field | Description |
|-------|-------------|
| `sent_id` | Sentence ID |
| `sentence` | Original Guaraní–Spanish text |
| `has_emoji` | Boolean indicating emoji presence |
| `lang_tags` | Token-level language ID list |
| `Formality` | Register label (*Formal* / *Informal*) |
| `Genre`, `Topic`, `Secondary_Topic` | Discourse/topic annotations |
| `sentence_len` | Token count per sentence |
| `total_spa`, `total_gua` | Token counts by language |

---

## Licensing & Citation

Both corpora are redistributed in **derived, annotated form** for research and non-commercial purposes only.

- **Original data sources:**
  - Bangor Miami Corpus - © Bangor University, ESRC Centre for Research on Bilingualism.
  - GUA-SPA Corpus - IberLEF 2023 shared task dataset.

Please cite both the **original resources** and our paper:

```bibtex
@LanguageResource{BangorMiami2014,
  title     = "{Bangor Miami Corpus} of Spanish--English Bilingual Speech",
  author    = "Deuchar, Margaret and Davies, Peredur and Herring, Jon and Parafita Couto, M. Carmen and Carter, Diana",
  year      = 2014,
  pid       = "https://bangortalk.org.uk",
  publisher = "ESRC Centre for Research on Bilingualism, Bangor University"
}

@LanguageResource{GUA-SPA2023,
  title     = "{GUA-SPA}: Guaraní--Spanish Code-Switching Corpus (IberLEF 2023)",
  author    = "Chiruzzo, Luis and Agüero-Torales, Marvin and Giménez-Lugo, Gustavo and Alvarez, Aldo and Rodríguez, Yliana and Góngora, Santiago and Solorio, Thamar",
  year      = 2023,
  pid       = "http://journal.sepln.org/sepln/ojs/ojs/index.php/pln/article/view/6563",
  publisher = "IberLEF 2023 Shared Task on Guaraní–Spanish Code-Switching Analysis"
}

