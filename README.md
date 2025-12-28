# 🎨 SketchToScale: GenAI Design Engine (PoC)
**Generative AI | Rapid Prototyping | Computer Vision**

![Status](https://img.shields.io/badge/Status-Proof_of_Concept-yellow?style=for-the-badge)
![Domain](https://img.shields.io/badge/Domain-Generative_Design-purple?style=for-the-badge)
![Tech](https://img.shields.io/badge/Model-Stable_Diffusion_%7C_ControlNet-blue?style=for-the-badge)

---

### 💼 Executive Summary
In product development, the "Gap of Fidelity" is a major bottleneck. Designers and PMs can sketch ideas in seconds, but rendering them into high-fidelity concepts takes hours using traditional CAD or Photoshop tools.

**SketchToScale** is a **Proof of Concept (PoC)** exploring how Generative AI can bridge this gap. This prototype demonstrates a pipeline that transforms rough hand-drawn sketches into photorealistic product renders using **Stable Diffusion** and **ControlNet** adapters, aiming to validate the feasibility of AI-assisted rapid prototyping.

---

### ❓ The Business Problem
* **Slow Iteration Cycles:** Waiting for 3D renders to validate a simple idea wastes valuable sprint time.
* **Communication Gaps:** "Napkin sketches" are often misinterpreted by stakeholders or engineering teams.
* **Resource Bottlenecks:** High-fidelity rendering requires expensive software and specialized talent.

---

### 💡 The Solution: AI-Assisted Rendering (Prototype)
I built an experimental pipeline that respects the *structure* of a user's drawing while using AI to hallucinate the *texture and lighting*.

| Feature | Technical Implementation | PM Value Proposition |
| :--- | :--- | :--- |
| **Structure Preservation** | <code>ControlNet (Canny/Scribble)</code> | Ensures the AI doesn't just make *any* image, but strictly follows the lines of the specific sketch. |
| **Style Transfer** | <code>Prompt Engineering</code> | Allows users to pivot styles instantly (e.g., "Cyberpunk Toaster" vs. "Minimalist Toaster") without redrawing. |
| **Feasibility Testing** | <code>Streamlit Interface</code> | A lightweight UI built to test user interaction flows and model latency. |

---

### 🖼️ Visual Proof (Input vs. Output)
*Demonstration of the underlying ControlNet capability used in this PoC.*

![Sketch to Image Example](public/generated_image.png)

*(Figure 1: ControlNet Scribble architecture demonstrating structural adherence.)*

---

### 🛠 Tech Stack
* **Core GenAI:** `Stable Diffusion v1.5`
* **Conditioning:** `ControlNet` (Scribble/Canny Edge Detection)
* **Backend:** `Python`, `PyTorch`
* **Frontend:** `Streamlit` (Prototype UI)

---

### 🚀 How to Run the Prototype
```bash
# Clone the repository
git clone https://github.com/skandvj/SketchToScale-GenAI-Design-Engine

# Install dependencies
pip install -r requirements.txt

# Launch the Interface
streamlit run app.py
## License
```

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.
