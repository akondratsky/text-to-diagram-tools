# Text-to-diagram tools

## Description

This repository is just a short introduction in the world of text-to-diagram tools. To try it on your own, checkout this repository, install required tools, described in the [extensions](#vscode-extensions) section, and follow [the list of the files](#files-in-this-repository).

## Comparison

You can take a look at the [Community list of comparisons between Text to Diagram tools](https://text-to-diagram.com/) to get a high-level understanding of differences between different engines. It supports comparison between D2, PlantUML, MermaidJS and GraphViz. 

- [**D2**](https://d2lang.com/tour/intro/) is the simplest one and probably the best for fast diagram prototyping. Has a minimum of functionality, but ELK layout engine is amazing, and makes complex diagrams really readable. It supports LaTeX, basic styling, markdown and even more.

- [**PlantUML**](https://plantuml.com/sitemap-language-specification) provides a lot of different features, and syntax
  - **AsciiMath** and **JLaTeXMath** notations to support mathematical expressions
  - **Creole** as a markup language
  - CSS-like styles
  - integration with [OpenIconic](https://icon-sets.iconify.design/oi/) to render icons
  - timing diagram syntax
  - use case diagram syntax
  - syntax for Gantt diagrams
  - syntax for mindmap diagrams
  - **nwdiag** for network diagrams
  - Extended Backus-Naur Form (EBNF) to specify the structure of formal languages
  - **Salt** to design website wireframe or page schematic or screen blueprints

- [**Mermaid**](https://mermaid.js.org/intro/) is a powerful tool to create diagrams and visualizations. Available as extension for vscode, as plugins for Confluence, as online tool, as JS library.
  - flowcharts (activity diagram)
  - sequence diagrams
  - class diagrams
  - state diagrams
  - entity relationship diagrams
  - Gantt diagrams
  - pie and quadrant charts
  - git diagram **(!)**
  - and others

- [**kroki.io**](https://kroki.io/) provides a unified API with support for a lot of platforms: _BlockDiag, SeqDiag, ActDiag, NwDiag, PacketDiag, RackDiag), BPMN, Bytefield, C4 (with PlantUML), D2, DBML, Ditaa, Erd, Excalidraw, GraphViz, Mermaid, Nomnoml, Pikchr, PlantUML, Structurizr, SvgBob, TikZ, UMLet, Vega, Vega-Lite, WaveDrom, WireViz... and more to come!_ All this support is available via [Markdown Kroki](https://marketplace.visualstudio.com/items?itemName=pomdtr.markdown-kroki) vscode extension


## vscode extensions

- [D2](https://marketplace.visualstudio.com/items?itemName=terrastruct.d2)
- [PlantUML](https://marketplace.visualstudio.com/items?itemName=jebbs.plantuml)
- [Mermaid Editor](https://marketplace.visualstudio.com/items?itemName=tomoyukim.vscode-mermaid-editor)
- [Markdown Kroki](https://marketplace.visualstudio.com/items?itemName=pomdtr.markdown-kroki) (you may need to set PlantUML server manually, see ["PlantUML server is mandatory"](https://github.com/qjebbs/vscode-plantuml/issues/255) issue)


## Files in this repository

- [workshop_d2_diagram.d2](./workshop_d2_diagram.d2) Empty file to conduct workshop and show basic principles of building diagrams with D2

- [drawio_sequence_diagram.drawio](./drawio_sequence_diagram.drawio) Example of a diagram created with draw.io service. To understand the pain of editing such diagrams, try to add one more request with activation between _dispatch 6_ and _dispatch 7_. It will take **a lot** of actions.

- [difficult_sequence_diagram.png](./difficult_sequence_diagram.png) Given this example it is really easy to understand than manual diagram drawing is not the solution if you want to edit diagrams.

- [hard_sequence_diagram.d2](./hard_sequence_diagram.d2) This example with the same complexity as **draw.io** diagram, but done with D2. You can try to add activation between _dispatch 6_ and _dispatch 7_ just with adding the code:
```
    D.anotherProcess -> E.activation
    E.activation -> D.anotherProcess: { style.stroke-dash: 2 }
```

- [hard_sequence_diagram.puml](./hard_sequence_diagram.puml) Almost the same diagram as previous, but created with PlantUML. This example shows that PlantUML has both more opportunities (like note on the same level) and drawbacks (it is impossible to draw some specific things)

- [diagram_types.d2](./diagram_types.d2) Regular block diagram, built with D2, represents types of UML diagrams which could be used to represent different aspects of a system. Uncomment one line to make the diagram even more beautiful. It also worth playing with different preview layouts (dagre and elk). You can play with [D2 styles](https://d2lang.com/tour/style) here

- [diagram_types.puml](./diagram_types.puml) The same block diagram with types of UML diagrams, which is made with PlantUML.

- [templates_flow.puml](./templates_flow.puml) Real-life example of diagram, result of architecture analysis of existing system. This example shows drawbacks of PlantUML layout engine.

- [templates_flow.d2](./templates_flow.d2) The same real-life example, built with D2. ELK engine demonstrates much better layout than Dagre

- [d2-shapes.d2](./d2-shapes.d2) Available basic shapes in D2. Rendered better with ELK.

- [d2-features-and-diagrams.d2](./d2-features-and-diagrams.d2) - available features and diagrams (icons, SQL tables etc)

- [kroki-markdown.md](./kroki-markdown.md) contains examples of diagrams included into the markdown, rendered with Markdown Kroki vscode extension

