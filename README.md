# 🔥 InYogeshwar AI Voice Cloner

**Clone Any Voice in Seconds** – A one‑click Google Colab notebook for training high‑quality voice conversion models using the **RVC (Retrieval‑based Voice Conversion)** framework.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/github/in-yogeshwar/rvc-voice-cloner/blob/main/InYogeshwar_AI_Voice_Cloner.ipynb](https://colab.research.google.com/drive/1Tyf6qRxl66CGnkWHTrNFDNykoCNMqpjS?usp=sharing))

---

## ✨ Features

- 🚀 **One‑click installation** – all dependencies are installed automatically in Colab.
- 🎙️ **Train on your own voice** – upload a clean vocal recording (3–10 minutes recommended).
- 🔁 **Resume training** – automatically continues from the last saved checkpoint.
- 💾 **Backup & restore** – save your model to Google Drive and load it later.
- 🎛️ **Pitch control** – adjust the pitch during inference (male↔female).
- 📦 **Pre‑trained models** – uses the official RVC pretrained weights for fast convergence.

---

## 📋 Requirements

- A **Google account** (to use Colab).
- A **GPU runtime** (T4 or V100 – Colab provides this for free).
- A **clean vocal audio file** (mono, 32 kHz, 3–10 minutes) – the longer, the better.

---

## 🚀 Getting Started

### 1. Open the notebook

Click the **Open In Colab** badge above, or directly copy the notebook code from this repository into a new Colab notebook.

### 2. Set GPU runtime

In Colab, go to **Runtime → Change runtime type → T4 GPU**.

### 3. Run the cells in order

- **Step 1 – Install & Cleanup** – downloads RVC and installs dependencies (takes ~5 min).
- **Step 2 – Upload Dataset** – upload your vocal recording.
- **Step 3 – Preprocess & Build Index** – converts the audio, extracts features, and builds the FAISS index.
- **Step 4 – Train Model** – set the number of epochs (200 is a good start) and start training.
- **Step 5 – Backup Model** (optional) – save your model to Google Drive.
- **Step 6 – Inference** – upload any speech file, adjust pitch, and get the converted audio.

### 4. Enjoy your cloned voice!

The converted audio will be played in the notebook, and you can download it.

---

## 🧪 Example

Assume you want to clone the voice of a male speaker named **Rahul**:

1. **Dataset**: Upload a 5‑minute WAV file of Rahul speaking clearly (no background music).  
   The notebook will convert it to the required format.

2. **Model name**: Set `model_name = "rahul_voice"` in the training cells.

3. **Training**: Run for 200 epochs. Loss values (`loss_mel`) will gradually drop.

4. **Backup**: After training, use the backup cell to save `rahul_voice.tar.gz` to Google Drive.

5. **Inference**: Upload a short audio file of a different speaker (e.g., a female voice). Set `pitch = 12` to convert it to Rahul’s voice.  
   The output will sound like Rahul speaking the same words.

---

## 📁 Repository Structure
.
├── InYogeshwar_AI_Voice_Cloner.ipynb # Main Colab notebook
├── README.md # This file
└── assets/ # (Optional) images for README

---

## 🛠️ Advanced Usage

- **Longer dataset**: If you have a 20‑minute recording, the model quality improves significantly. You can reduce `epochs` to 100–150.
- **Out of memory**: If you encounter CUDA out of memory, lower the `batch_size` to 4 or 2.
- **Resume training**: Just run the training cell again – it will automatically detect existing checkpoints and continue.

---

## 📜 License

This project uses the [RVC](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) framework, which is open‑source.  
The notebook is provided under the **MIT License**.

---

## 🙏 Acknowledgements

- [RVC Project](https://github.com/RVC-Project/Retrieval-based-Voice-Conversion-WebUI) – for the amazing voice conversion technology.
- [Bahaa AI](https://www.youtube.com/@BahaaAI) – for the original Colab tutorial that inspired this notebook.
- [Google Colab](https://colab.research.google.com/) – for providing free GPU resources.

---

## ⚠️ Important

**Use this tool responsibly.** Only clone voices you have explicit permission to use. Misuse of voice cloning technology may violate privacy laws and terms of service.

---

## 📧 Contact

- 🌐 Website: [inyogeshwar.co.in](https://www.inyogeshwar.co.in)
- 📺 YouTube: [@in_yogeshwar](https://www.youtube.com/@in_yogeshwar)
- 📸 Instagram: [@in_yogeshwar](https://www.instagram.com/in_yogeshwar/)

Happy voice cloning! 🎤🔥
