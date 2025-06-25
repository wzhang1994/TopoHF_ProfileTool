# TopoHF_ProfileTool
Extracts and visualizes heat flow and topography data near a defined geological profile. 

## 🔧 Toolchain

- **GMT (Generic Mapping Tools)** ≥ 6.4
- **Shell**: `zsh` (or bash with slight modification)

## 📁 Input Files

- `@earth_relief_01m`: Global topographic grid (auto-downloaded by GMT if not present)
- `HF.xyz`: ASCII file containing XYZ data (e.g., heat flow points)

## 📤 Output Files

- `ALL.zwt`: All heat flow measurements
- `ProfileAB.dat`: Heat flow measurements to be plotted
- `DistanceAB.dat`: Main processed profile data
  - Columns: distance along profile (km), perpendicular distance from profile (km), Z value
- `*.ps`: Final profile plot (PostScript)

## ⚠️ Notes

1. The middle Point B could overlap to enable a single-profile mode.
2. Requires GMT modules such as `project`, `grdtrack`, `psxy`, `grdimage`, etc.

## 🗂️ Example Usage

```bash
chmod +x *.job
zsh 0step1.job
zsh 0step2AB.job
```
