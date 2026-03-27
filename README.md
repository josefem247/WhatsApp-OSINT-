# WhatsApp OSINT Toolkit

## Overview
This toolkit provides modular workflows for parsing, exporting, and investigating WhatsApp and social media data. It is designed for transparency, reproducibility, and stakeholder engagement, with outputs in multiple formats (CSV, GeoJSON, media index, deleted logs, network graphs, keyword indexes).

## Features
- **Cross-platform auto-detection** of WhatsApp and social media exports
- **Modular parsers** for chat logs, media, and metadata
- **Export options**: CSV, JSON, GeoJSON, and graph structures
- **Investigation aids**: keyword indexes, deleted message logs, and network mapping
- **Stakeholder-ready documentation** with layered technical and executive summaries

## Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/yourusername/WhatsApp-OSINT.git
cd WhatsApp-OSINT
pip install -r requirements.txt

import os
import subprocess
import shutil

def install_requirements():
    """Install dependencies from requirements.txt if present."""
    if os.path.exists("requirements.txt"):
        print("[*] Installing Python dependencies...")
        subprocess.run(["pip", "install", "-r", "requirements.txt"])
    else:
        print("[!] No requirements.txt found, skipping dependency install.")

def run_main():
    """Run the main toolkit script."""
    entry_file = "main.py"  # change if your entry point has a different name
    if os.path.exists(entry_file):
        print(f"[*] Running {entry_file}...")
        subprocess.run(["python", entry_file])
    else:
        print(f"[!] {entry_file} not found. Please update run_toolkit.py with the correct entry file.")

def export_results():
    """Move results to shared storage for easy access."""
    results_dir = "results"
    target_dir = "/storage/emulated/0/Documents/"
    if os.path.exists(results_dir):
        print("[*] Exporting results to shared storage...")
        for file in os.listdir(results_dir):
            src = os.path.join(results_dir, file)
            dst = os.path.join(target_dir, file)
            try:
                shutil.move(src, dst)
                print(f"    Moved {file} → {target_dir}")
            except Exception as e:
                print(f"    Could not move {file}: {e}")
    else:
        print("[!] No results directory found, skipping export.")

if __name__ == "__main__":
    install_requirements()
    run_main() 
    export_results() 
    print("[✓] Workflow complete.")

git add README.md
git commit -m "Update README with Termux wrapper instructions"
git push origin josefem247_1
