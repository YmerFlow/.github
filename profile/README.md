# Ymerflow — Cloud-Native Geophysics

Browser-based AEM and magnetic survey processing, inversion, and pipeline automation — no Windows install, no per-seat licenses, no black-box algorithms.

Ymerflow replaces desktop-bound geophysics tools with a reproducible, versioned workflow platform that runs in any browser. Processing pipelines are defined as visual DAGs, executed in Kubernetes containers, and stored in per-project cloud storage so results are always reproducible. The inversion core is [SimPEG](https://simpeg.xyz/) (GPL v3) — peer-reviewed, auditable, and extensible.

| Process graph view | Process editor |
|---|---|
| ![Flow view showing process graph and 3D resistivity curtain](https://raw.githubusercontent.com/YmerFlow/Ymerflow/master/screenshots/ymerflow_ui_screenshot%20(1).png) | ![Process editor with 3D resistivity curtain](https://raw.githubusercontent.com/YmerFlow/Ymerflow/master/screenshots/ymerflow_ui_screenshot.png) |

![AEM inversion comparison — AGF reference (top) vs. Ymerflow result (bottom)](https://raw.githubusercontent.com/YmerFlow/Ymerflow/master/screenshots/published-vs-ymerflow-inversion.png)

## Features

<div class="feature-card" markdown="1">

### Visual Pipeline Editor
🔀 DAG-based process graph showing dependencies and data flow  
🖱️ Drag-and-drop interface with resizable splits, tabs, and popout windows for multi-monitor workflows  
📡 Real-time log streaming via WebSocket  
💰 Usage-based billing with upfront cost estimates per job  
💾 Persistent layout configuration  

</div>

<div class="feature-card" markdown="1">

### Geophysics Processing & Inversion
🛜 AEM (TEM) processing and 1D/3D inversion via SimPEG — open, peer-reviewed algorithms  
🧲 Magnetic processing, equivalent-source gridding, and 3D magnetic inversion  
🔌 Plugin process types: any Python `schema()` + `run()` pair registers as a new process type, so custom algorithms slot in without forking the platform  

</div>

<div class="feature-card" markdown="1">

### Scientific Visualization
🗻 3D resistivity curtains along flightlines and voxel grids for 3D inversion results  
🌐 Geographic map view with EPSG coordinate axes and flightline plotting  
📊 Extensible plot element system with unit-aware axis matching  

</div>

## Source code

The [main repo](https://github.com/YmerFlow/Ymerflow) contains the orchestration to install the system on your machine. However, each component, such as our [SimPEG fork](https://github.com/Ymerflow/simpeg), the [AEM processing pipeline](https://github.com/YmerFlow/ymerflow-processing) and the [Gladly plotting framework](https://github.com/YmerFlow/gladly) etc, is available from a separate repo.
