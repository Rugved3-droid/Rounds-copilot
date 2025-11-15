# Rounds-copilot
An AI powered approach to capturing and enhancing spontaneous clinical teaching

# Rounds Copilot: AI-Powered Bedside Teaching Assistant

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An AI-powered educational tool that automatically captures spontaneous bedside teaching during clinical rounds and converts it into structured, evidence-based learning materials with integrated formative assessment.

## Overview

Rounds Copilot addresses the ephemeral nature of bedside teaching by:
- *Transcribing* clinical conversations using speech recognition
- *Extracting* discrete teaching kernels from unstructured dialogue
- *Classifying* content as guideline-backed evidence vs. clinical pearls
- *Linking* teaching points to published guidelines and literature
- *Generating* multiple-choice questions with detailed rationales

## Key Features

- *Voice-to-Text Processing*: Automatic transcription of attending-resident teaching interactions
- *Teaching Kernel Extraction*: AI identifies educational content from clinical dialogue
- *Evidence Classification*: Distinguishes guideline-backed recommendations from experiential wisdom
- *Guideline Cross-Referencing*: Links content to ACC/AHA, ESC, and other authoritative sources
- *Formative Assessment*: Auto-generates MCQs with clinical vignettes and evidence-linked rationales
- *Institutional Knowledge Preservation*: Creates searchable repository of faculty teaching patterns

## Video Demonstration

📺 Watch the system in action: (https://youtu.be/p3KiE4b_NXA)

## Installation

### Prerequisites

- Python 3.8+
- OpenAI API key
- Microphone access (for live recording) or audio files

### Setup

1. Clone the repository:
bash
git clone https://github.com/[Rugved3-droid]/rounds-copilot.git
cd rounds-copilot


2. Install dependencies:
bash
pip install -r requirements.txt


3. Set up your OpenAI API key:
bash
export OPENAI_API_KEY='your-api-key-here'


4. Run the application:
bash
streamlit run app.py


## Requirements


streamlit>=1.24.0
openai>=1.0.0
python-dotenv>=1.0.0
audio-recorder-streamlit>=0.0.8


## System Architecture


Audio Input → Whisper ASR → Text Transcription → GPT-4 Processing
                                                        ↓
                                              ┌─────────┴─────────┐
                                              ↓                   ↓
                                    Teaching Kernel         Evidence
                                      Extraction          Classification
                                              ↓                   ↓
                                              └─────────┬─────────┘
                                                        ↓
                                              Guideline Linking
                                                        ↓
                                              MCQ Generation
                                                        ↓
                                              Interactive Output


## Usage

### Recording a Teaching Session

1. *Start Recording*: Click the microphone button to begin capturing audio
2. *Conduct Teaching*: Engage in natural attending-resident teaching dialogue
3. *Stop Recording*: End the session when teaching is complete
4. *Process Audio*: System automatically transcribes and analyzes content
5. *Review Output*: Examine extracted teaching kernels, evidence links, and generated MCQs

### Example Teaching Scenario

*Input*: Attending discusses acute pericarditis management with resident

*Output*:
- 7 teaching kernels extracted
- 4 classified as guideline-backed (with citations)
- 3 classified as clinical pearls
- MCQs generated testing key concepts
- Links to ESC Guidelines, COPE trial, FDA information

### Output Components

1. *Teaching Kernels*: Discrete educational points with evidence classification
2. *Evidence-Based References*: 
   - Clinical guidelines (ESC, ACC/AHA)
   - Landmark trials (COPE, etc.)
   - Drug information (FDA prescribing details)
3. *Multiple-Choice Questions*:
   - Clinical vignette stems
   - 5 answer options with plausible distractors
   - Detailed rationales linking to source teaching
4. *Interactive Interface*: Immediate feedback on answer selection

## Educational Theory Foundation

Rounds Copilot is grounded in established learning science:

- *Spaced Repetition*: Allows review of content days after initial exposure
- *Retrieval Practice*: MCQs strengthen long-term retention
- *Cognitive Load Reduction*: Learners focus on clinical reasoning, not note-taking
- *Evidence-Based Learning*: Explicit links to authoritative sources
- *Critical Appraisal*: Distinguishes evidence from expert opinion

## Technical Considerations

### Audio Quality
- Background noise impacts transcription accuracy
- Recommended: Directional microphones or wearable recording devices
- Speaker diarization works best with distinct voice characteristics

### AI Processing
- Uses GPT-4 with low temperature settings for consistency
- Custom prompts optimized for medical education content
- Processing time: ~2-3 minutes for 10-minute recording

### Privacy & Compliance
- No permanent storage of patient identifiers
- Audio processed via OpenAI API
- HIPAA compliance required for clinical deployment
- Explicit consent needed for patient encounter recording

## Important Disclaimers

⚠️ *This tool is for educational and research purposes.*

- Proof-of-concept system requiring validation before clinical use
- AI-generated MCQs require faculty review for accuracy
- Does not replace faculty teaching or clinical judgment
- Privacy and consent protocols essential for real-world deployment
- Current version captures verbal content only (not physical exam, imaging, etc.)

## Limitations

- Demonstrated with simulated scenarios, not real clinical encounters
- No formal validation of learner outcomes yet conducted
- Verbal teaching only; non-verbal content not captured
- AI outputs are probabilistic and may contain errors
- Requires internet connectivity for API access

## Future Directions

- Real-world validation in clinical teaching settings
- Learner outcome assessment studies
- Integration with learning management systems
- Multimodal input support (ECG, imaging)
- Specialty-specific adaptations beyond cardiology
- Comparative studies vs. general-purpose AI tools

## Citation

If you use this tool in your research, please cite:

bibtex
@article{parmar2025rounds,
  title={Preserving the Bedside: An AI-Powered Approach to Capturing and Enhancing Spontaneous Clinical Teaching},
  author={Parmar, Rugved and Eldawoud, Daoud and Fahim, MD and Budzikowski, Adam},
  journal={Journal of Medical Systems},
  year={2025},
  note={Manuscript submitted for publication}
}


## Author

- *Rugved Parmar, MD* - SUNY Downstate Health Sciences University

## Contact

For questions, collaboration inquiries, or implementation support:
- Email: Rugved.parmar@downstate.edu
- Institution: SUNY Downstate Health Sciences University, Brooklyn, NY

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- OpenAI for Whisper and GPT-4 APIs
- Medical education researchers whose work informed the theoretical foundation
- Clinical guideline committees (ACC/AHA, ESC) for evidence-based resources
- Faculty and residents who inspired this educational innovation

---

*Note*: This is a proof-of-concept system. Real-world validation studies are needed to assess educational impact, user acceptance, and comparison to existing approaches before widespread clinical implementation.
