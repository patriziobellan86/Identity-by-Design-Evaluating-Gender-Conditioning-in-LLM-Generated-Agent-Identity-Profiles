# Identity-by-Design-Evaluating-Gender-Conditioning-in-LLM-Generated-Agent-Identity-Profiles
Repository of the paper "Identity by Design? Evaluating Gender Conditioning in LLM-Generated Agent Identity Profiles" published in the workshop Identity Aware AI at ECAI 2025.

The descriptions are divided in the following files, according to their experimental condition (i.e. the gender assigned to the psychologist agent):

• `PoE_Unconstrained.json` – No gender assigned

• `PoE_Female.json` – Female psychologist

• `PoE_Male.json` – Male psychologist

• `PoE_Nonbinary.json` – Non-binary psychologist 

To correctly parse and utilize this data, please refer to the table below, which summarizes the fields and data types for each JSON record:


| Field                      | Type     | Description                                                                                                                                                                                                                                                                               |
| -------------------------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **experimental_condition** | `string` | Indicates the gender assignment condition of the psychologist in the experiment. Possible values:<br>• `Experiments` – No gender assigned<br>• `ExperimentsFemale` – Female psychologist<br>• `ExperimentsMale` – Male psychologist<br>• `ExperimentsNonbinary` – Non-binary psychologist |
| **dataset**                | `string` | The reasoning dataset.                                                                                                                                                                                                    |
| **desc_framework**         | `string` | The psychological description framework used (e.g. `Big Five Personality Traits`).                                                                                                                                                                                     |
| **model**                  | `string` | The underlying LLM used to generate the description (e.g., `claude-3.7-sonnet`).                                                                                                                                                                                                            |
| **role**                   | `string` | The assigned role within the *PoE* framework.                                                                                                                                                                                   |
| **name**                   | `string` | The name of the simulated agent.                                                                                                                                                                                                                    |
| **description**            | `string` | The full generated text describing the agent.                                                                                                                                                                              |
| **inferred_gender**        | `string` | The gender inferred from the generated text using `gpt-4o-mini`. Possible values: `male`, `female`, `nonbinary`, `unknown`.                                                                                                                                                            |
| **polarity**               | `float`  | Sentiment polarity score (computed via **TextBlob**). Ranges from -1 (negative) to +1 (positive).                                                                                                                                                                                         |
| **subjectivity**           | `float`  | Subjectivity score (computed via **TextBlob**). Ranges from 0 (objective) to 1 (subjective).                                                                                                                                                                                              |
| **sentiment**              | `string` | Simplified sentiment classification derived from polarity: `Positive`, `Neutral`, or `Negative`.                                                                                                                                                                                    |
