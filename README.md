# SlizzAi Codex v3.5

A next-generation AI-driven creative engine that bridges text prompts, procedural 3D modeling, physics simulation, animation styling, and real-time Unreal Engine integration—all behind an interactive GUI.

---

## Features

- Visual prompt styling with tactical, anime, cinematic, or custom modes  
- Self-learning 3D mesh generation and iterative refinement  
- Procedural organism evolution based on species type and environment  
- Seed-based character randomization for rapid variation  
- Real-world pose retargeting via mocap-style actions  
- Destruction simulation with fracture patterns and physics  
- Energetic weight control and force application for dynamic assets  
- Energy VFX framework (Power Equator) for super-ability effects  
- Live Unreal Engine sync (connect & push scene data)  
- Tkinter GUI with live sliders for mass, force (X/Y/Z), and energy intensity  
- Single-script production-ready codebase, easily extendable  

---

## Architecture Overview

| Module                     | Responsibility                                           |
|----------------------------|----------------------------------------------------------|
| EmotionEngine              | Detects prompt tone and adapts styling                  |
| PersonaShifter             | Applies named style transformations to text prompts     |
| SelfLearningModeler        | Generates and refines 3D meshes from stylized prompts   |
| OrganismAnalyzer           | Evolves species meshes based on environment profiles    |
| CharacterRandomizer        | Produces trait variations using seeded ranges           |
| PoseStyler                 | Applies action-based poses to meshes                    |
| DestructionSimulator       | Simulates mesh fracturing with configurable patterns    |
| EnergeticWeightController  | Adjusts mass and applies force vectors                  |
| PowerEquator               | Generates energy-based VFX tied to defined abilities    |
| UnrealLiveBridge           | Manages bi-directional sync with Unreal Engine          |
| SlizzAiGUI (Tkinter)       | Interactive interface with live parameter sliders       |

---

## Installation

1. Clone this repository:  
   ```bash
   git clone https://github.com/your-org/SlizzAiCodex.git
   cd SlizzAiCodex
   ```

2. Create and activate a Python virtual environment:  
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # on Windows use `venv\Scripts\activate`
   ```

3. Install dependencies (only standard library modules used in prototype):  
   ```bash
   pip install tkinter
   ```

---

## Usage

1. Configure `ConfigSchema` parameters in `main.py` or your custom script.  
2. Define a `PromptSchema` object with your prompt text, style, species, and initial physics/VFX settings.  
3. Run the GUI application:  
   ```bash
   python main.py
   ```

4. Adjust the **Mass**, **Force (X/Y/Z)**, and **Energy Intensity** sliders in real time.  
5. Click **Run Pipeline** to generate and display results in the console panel.  
6. (Optional) Integrate with Unreal Engine by implementing the bridge’s `connect` and `push` methods.

---

## Example

```python
from main import ConfigSchema, PromptSchema, CodexOrchestrator, SlizzAiGUI

config = ConfigSchema(
  styles={"cyberpunk":"assets/styles/cyber.json","anime":"assets/styles/ani.json"},
  model={"type":"slizz-mesh-v1"},
  randomizer={"height":[1.6,2.0],"strength":[10,100]},
  physics_presets={"steel":{"density":7850},"organic":{"density":1200}},
  mocap_library=["run","jump","strike"],
  vfx_profiles={"flare":"cyan","shockwave":"magenta"},
  ue_project="C:/SlizzAi/UnrealProject"
)

prompt = PromptSchema(
  prompt="Cyber ninja vaults over collapsing drones!",
  style="cyberpunk",
  seed=2025,
  species_type="NeoHuman",
  environment_profile={"biome":"urban","hazard":"electro-storm"},
  action_type="vault",
  fracture_pattern={"type":"radial","segments":8},
  new_mass=5.5,
  force_vector=[0.0,-9.8,0.0],
  energy_intensity=3.7,
  ability_set={"shadow_blade":"slice","storm_core":"burst"}
)

orchestrator = CodexOrchestrator(config)
app = SlizzAiGUI(orchestrator, prompt)
app.mainloop()
```

---

## Contributing

- Fork the repo and create a feature branch  
- Implement new modules or improve existing ones (fill in UE bridge, add shader support, etc.)  
- Write tests for new functionality  
- Submit a pull request against `main` with detailed changelog entries  

---

## License

This project is released under the MIT License. See `LICENSE` for details.

# SlizzAi 3.3 – Advanced AI Plugin for Unreal Engine  

SlizzAi 3.3 brings powerful AI-driven functionality to Unreal Engine, enabling seamless integration with creative workflows. Designed with precision, it enhances automation, procedural generation, and cinematic depth while maintaining performance efficiency.

## 🚀 Features  
- **AI-Powered Integration** – Smooth Unreal Engine compatibility for advanced automation.  
- **Procedural Generation** – Dynamic world-building with intelligent AI-driven scene construction.  
- **Licensing & Security** – Robust serial coding and electronic signature validation for secure distribution.  
- **Optimized Performance** – Engineered for efficiency without compromising creative flexibility.  
- **Custom Extensions** – Expand functionality with Python-driven modules tailored for unique use cases.  

## 🛠 Installation  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/your-repo/slizzai.git  
   cd slizzai  
   ```  
2. Install dependencies:  
   ```bash  
   pip install -r requirements.txt  
   ```  
3. Integrate with Unreal Engine via the plugin settings.  

## 🔑 Licensing & Usage  
SlizzAi 3.3 is released under a proprietary license with individual serial coding and electronic signatures. Please review the licensing agreement before use.  

## 📖 Documentation  
Comprehensive guides and API references are available in the `/docs` directory.  

## 🌟 Contribution  
Contributions are welcome! Submit issues, feature requests, or pull requests to help improve SlizzAi.
