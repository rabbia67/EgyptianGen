# 🏺 EgyptianGen — Ancient Egyptian Text-to-Image Generation System

**EgyptianGen** is a specialized AI-based **text-to-image generation system** designed to produce **historically accurate** and **culturally informed** imagery of Ancient Egypt.  
By integrating **domain-specific academic knowledge** with **state-of-the-art generative models**, it serves as a tool for **education**, **research**, and **artistic exploration** of Egyptian heritage.

---

## 📂 Repository Structure

```plaintext
EgyptianGen/
│
├── EgyptionGen_Computer_Vision_Project.ipynb   # Main Jupyter Notebook implementation
├── Reproduced Paper.pdf                        # Full research paper explaining the system
├── egyptian_academic_database.json             # Curated cultural database of Ancient Egypt
├── medium_article_link.txt                     # Link to project article on Medium
└── README.md
```

---

## 🧭 System Overview

EgyptianGen features a **multi-stage pipeline**:

1. **PDF Processing** — Extracts text and images from Egyptology PDFs to build a knowledge base.
2. **Egyptian Academic Cultural Database (EACD)** — Structured JSON with curated data on:
   - Deities & pharaohs  
   - Commoner archetypes  
   - Artistic conventions  
   - Architectural elements  
   - Funerary practices
3. **Figure Classification** — Uses a SentenceTransformer model to identify figures from prompts.
4. **Prompt Enhancement** — Employs Flan-T5 to enrich prompts with cultural and historical details.
5. **Image Generation** — Utilizes FLUX models (via Replicate API) to create accurate images.
6. **User Interface** — Built with Gradio for web use and supports Colab/Jupyter execution.

---

## 🛠️ Methodology

- **Environment Setup**: Works locally or on Google Colab.
- **Libraries**: Uses Python packages including `transformers`, `torch`, `sentence-transformers`, `pytesseract`, `pymupdf`, `Pillow`, and `gradio`.
- **API Integration**: Requires a `REPLICATE_API_TOKEN` for FLUX model access.
- **Data Processing**: Automates OCR and image extraction from academic PDFs.
- **Knowledge Base**: Stores structured, detailed entries for accurate prompt enrichment.
- **Generation Process**:
  1. Classify figure/theme.
  2. Retrieve relevant context.
  3. Enhance prompt with visual and historical accuracy.
  4. Generate image via FLUX.
  5. Display enhanced prompt, academic context, and final image.

---

## 🎯 Example Capabilities

- **Deity Depictions**: Isis, Ra-Horakhty, Anubis, Thoth
- **Pharaonic Scenes**: Warrior Pharaohs, offering rituals
- **Cultural Scenes**: Scribes at work, funerary processions
- **Architectural Elements**: Temples, tombs, obelisks

---

## 📊 Results & Discussion

- **FLUX-dev**: Higher detail and historical fidelity  
- **FLUX-schnell**: Faster generation (~30-40 seconds quicker) with slightly less detail
- **Caching**: Model and embedding caching improves repeated use
- **Limitations**:
  - Dependent on database quality
  - Possible OCR errors
  - Model biases and knowledge scope limitations

---

## 🔮 Future Work

- Expand database with more archetypes & variations
- Fine-tune models on Egyptology-specific datasets
- Add user feedback mechanisms
- Support multi-language prompts
- Enable style controls and reference image guidance
- Explore 3D reconstruction from descriptions

---

## 📌 Potential Applications

- **Education**: Interactive history lessons
- **Research**: Visualizing scholarly hypotheses
- **Art & Design**: Historically inspired content creation
- **Museums**: Interactive and dynamic exhibition visuals
- **Media**: Unique, accurate content for documentaries & games

---

## 🚀 How to Run

1. **Clone the repo**:
   ```bash
   git clone https://github.com/rabbia67/EgyptianGen.git
   cd EgyptianGen
   ```
2. **Open Notebook**:
   ```bash
   jupyter notebook EgyptionGen_Computer_Vision_Project.ipynb
   ```
3. **Set API Key**:
   - Add `REPLICATE_API_TOKEN` to `secrets.json` or input when prompted.
4. **Run cells** in order to:
   - Load database
   - Process PDFs
   - Classify figure
   - Enhance prompt
   - Generate image

---

## 📄 License
For **educational and research purposes** only. Please cite the paper if you use EgyptianGen in your work.
