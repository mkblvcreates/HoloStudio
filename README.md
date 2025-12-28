<a style="float:right" href="https://youtu.be/1CLfB9cETWg" target="_blank">
  <img alt="HoloStudio Promotional Video" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/thumbnail.png" width="100%"/>
</a>

## Overview

Presenting Holographic Studio, a **volumetric video capturing and production system** for performance capture, visible from any perspective in virtual environments. 
This technology not only finds a natural application under the entertainment industry such as video-games and remote concerts, but also extends itself to other industries such as sports, fashion, culture, remote communication and education, military and medical training, among others. 

Holographic Studio, or HoloStudio for short, was born as a joint initiative between [University of Aveiro](https://www.ua.pt/) and [VR360](https://www.vr360.pt) and composes the work for my MSc. thesis in Informatics Engineering, year 2020/2021. This dissertation aims at reducing the gap between this technology, typically characterized by expensive hardware, scarce availability or high usage costs, and small and medium-sized companies that would benefit with the increase in immersion of their content. 

The proposed infrastructure resorts to RGB-D sensors to capture depth data and integrates 3D data processing algorithms to clean and replicate live action performances to be viewed in immersive virtual spaces. The implemented architecture provides a solid basis to future innovations on the photorealism of captures, in a scalable and replicable way.

## Capture Studio

The selected RGB-D camera was [Azure Kinect](https://github.com/Microsoft/Azure-Kinect-Sensor-SDK), synchronized through a combination of daisy-chain hardware connection and a custom software algorithm for refinement.
Calibration is done through a semi-automatic process, with key point manual selection for global alignment and the use of ICP for refinement.

Camera placement characteristics, including height, angle, orientation and distance, were all studied for results optimization.
The final capture studio, with custom lighting conditions, is highly portable and replicable.

<img alt="HoloStudio Multi-camera Synchronization Image 1" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/multicam-sync-daisychain.png" width="49%"> <img alt="HoloStudio Multi-camera Synchronization Image 2" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/multicam-placement.png" width="49%">

<img alt="HoloStudio Capture Studio Image 1" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/studio-1.png" width="49%"> <img alt="HoloStudio Capture Studio Image 2" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/studio-2.png" width="49%">

## Processing & Visualization

Source videos from all RGB-D cameras are fed as input and through a multi-step processing pipeline that includes:
- Input Validation
- Image Processing
- Point-Cloud Alignment & Processing
- Surface Reconstruction
- Texturing
- Exporting

Image processing, using flying-pixel removal and maximum range techniques (left) and histogram matching and color transfer algorithms (right), applied to a preview capture:

<img alt="Image Filtering 1" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/processing-flying-pixel-removal.png" width="49%"> <img alt="Image Filtering 2" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/processing-color-filter.png" width="49%">

Point-cloud alignment (left) and segmentation (right) using custom algorithms and standard processes (e.g. DBSCAN clustering), applied to a preview capture:

<img alt="Point-cloud Alignment" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/processing-alignment.png" width="49%"> <img alt="Point Cloud Segmentation" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/processing-segmentation.png" width="49%">

Poisson surface reconstruction, applied to a preview capture:

<img alt="Point-cloud Alignment" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/processing-surface-reconstruction.png" width="100%">

Visualization is done through a custom-developed [Unity](https://unity.com/) plugin, capable of real-time rendering of volumetric captures done through HoloStudio.

![banner](https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/unity-1.gif)

## Documentation & Citation

The full thesis is available in Portuguese at University of Aveiro's [Institutional Repository](https://ria.ua.pt/handle/10773/32261) or at my [ResearchGate Profile](https://www.researchgate.net/publication/353390434_HoloStudio_Volumetric_Video_Production_Tool_for_Immersive_Applications_MSc_Thesis_Informatics_Engineering_University_of_Aveiro).
Short version presentation, written in English, is available in PowerPoint format [here](https://github.com/FilipeLopesPires/HoloStudio/blob/main/docs/ThesisPresentation.pptx).
Promotional video also available on [YouTube](https://youtu.be/1CLfB9cETWg).

If you find this work useful, please cite:

```bibtex
@phdthesis{phdthesis,
  author = {Pires, Filipe},
  year = {2021},
  month = {07},
  pages = {},
  title = {HoloStudio: Volumetric Video Production Tool for Immersive Applications (MSc. Thesis Informatics Engineering, University of Aveiro)}
}
```

## Credits & Acknowledgments

I am the author of all work here presented, from the proprietary source code and dedicated infrastructure setup to the documentation, thesis and promotional video.
Hardware used during preliminary testing was offered by research institutions IEETA, IT and INESCTEC. 

This work could not have been done without the guidance of professors [Paulo Dias](https://github.com/pmdjdias) and [Miguel Oliveira](https://github.com/miguelriemoliveira).
Special thanks to Marcelo Silva and the entire VR360 team.

For further information, feel free to reach out.

<img alt="VR360 Team 2021" src="https://github.com/FilipeLopesPires/HoloStudio/blob/main/img/team.png" width="100%"/>
