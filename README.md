# LifelongCrossNav Project Page

<div align="center">

## Persistent 3D Semantic Memory for Cross-Floor Multi-Object Navigation

[Project Page](https://flageval-baai.github.io/LifelongCrossNavPage/) · **Paper: Coming Soon** · **Code: Coming Soon** · [Dataset](https://drive.google.com/file/d/1mZOn_BVWHqdp4kYCygWvf9I-z0IEl3Lc/view)

</div>

![Conceptual illustration of LifelongCrossNav](assets/figure/overall_illustration.png)

This repository hosts the official project website for **LifelongCrossNav**, a framework for sequential multi-object navigation in unknown multi-floor environments. LifelongCrossNav maintains a persistent sparse 3D semantic memory across consecutive object-goal subtasks, allowing the agent to reuse accumulated geometry, traversability, and vision-language information while navigating between floors.

The project also introduces **HM3D-MFMON**, a benchmark for sequential Multi-Floor Multi-Object Navigation built on HM3D scenes.

## Highlights

- **HM3D-MFMON benchmark:** 927 three-goal episodes from 36 multi-floor HM3D scenes, including 288 Cross-Floor-Required episodes.
- **Persistent 3D semantic memory:** goal-independent vision-language features and support-aware geometric states are accumulated in a shared sparse voxel map.
- **Cross-floor navigation:** stair-aware perception, frontier selection, and mode-aware 3D planning support navigation between floors.
- **Historical semantic retrieval:** History POIs reuse previously observed semantic evidence to improve the path efficiency of later object-goal subtasks.

## System Overview

![Overview of LifelongCrossNav](assets/figure/framework.png)

Given RGB-D observations, the agent pose, and the current goal text, LifelongCrossNav jointly updates a support-aware 3D voxel map and persistent 3D semantic memory. A unified navigation policy selects among Basic Frontiers, Stair Frontiers, History POIs, and Live POIs, and performs mode-aware planning for exploration, stair traversal, POI navigation, and final object approach.

## Project Resources

| Resource | Link |
| --- | --- |
| Project page | [flageval-baai.github.io/LifelongCrossNavPage](https://flageval-baai.github.io/LifelongCrossNavPage/) |
| Paper | Coming soon |
| Source code | Coming soon |
| HM3D-MFMON dataset | [Google Drive](https://drive.google.com/file/d/1mZOn_BVWHqdp4kYCygWvf9I-z0IEl3Lc/view) |

## Authors

Zehui Li<sup>1</sup>, Zihao Sun<sup>1</sup>, Jiawei Xu<sup>1</sup>, Zheqi He<sup>2</sup>, Xiaoqiang Zhang<sup>1</sup>, Jing-Shu Zheng<sup>2</sup>, Lu Liu<sup>2</sup>, Dahui Gao<sup>2</sup>, and Xiuwan Chen<sup>1</sup>

<sup>1</sup> Peking University  
<sup>2</sup> Beijing Academy of Artificial Intelligence

## Local Preview

The website is implemented as a dependency-free static site. To preview it locally:

```bash
cd /path/to/LifelongCrossNavPage
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Using a local HTTP server is recommended because browser behavior for video and other assets can differ when `index.html` is opened directly through a `file://` URL.

## Repository Structure

```text
LifelongCrossNavPage/
├── index.html                 # Page content and semantic structure
├── styles.css                 # Layout, responsive design, and visual styling
├── script.js                  # Navigation, reveal effects, and citation copy action
├── .nojekyll                  # Disables Jekyll processing on GitHub Pages
└── assets/
    ├── favicon.svg
    ├── figure/                # Conceptual, framework, and result figures
    ├── table/                 # Quantitative result tables
    └── video/                 # Cross-floor navigation demonstrations
```

## Deployment

This repository is designed to be published directly with GitHub Pages:

1. Push the website files to the `main` branch.
2. Open the repository's **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch and `/(root)` directory.
5. Save the configuration and wait for the Pages deployment to complete.

The deployed website will be available at:

```text
https://flageval-baai.github.io/LifelongCrossNavPage/
```

## Updating Release Links

The paper and source-code buttons currently use release placeholders. After public release, update the corresponding links in:

- `index.html`, for the website buttons and BibTeX entry;
- this `README.md`, for the resource links and citation;
- any Open Graph metadata used for link previews.

## Citation

The final BibTeX entry will be added after the paper becomes publicly available.

```bibtex
@article{li2026lifelongcrossnav,
  title   = {LifelongCrossNav: Persistent 3D Semantic Memory for
             Cross-Floor Multi-Object Navigation},
  author  = {Li, Zehui and Sun, Zihao and Xu, Jiawei and He, Zheqi and
             Zhang, Xiaoqiang and Zheng, Jing-Shu and Liu, Lu and
             Gao, Dahui and Chen, Xiuwan},
  journal = {arXiv preprint arXiv:XXXX.XXXXX},
  year    = {2026}
}
```

## License

The license for the project page, source code, and HM3D-MFMON annotations will be specified with the public release. Third-party assets and datasets remain subject to their respective licenses.
