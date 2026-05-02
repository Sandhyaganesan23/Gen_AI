```mermaid
flowchart TD
    A["💬 Input<br/>The cat sat on the mat"] --> B["🔢 Tokenization"]
    B --> C["🧊 Token Embeddings"]
    C --> D["📍 Positional Encoding"]
    D --> T

    B -.-> N1["Tokens:<br/>&quot;The&quot;, &quot;cat&quot;, &quot;sat&quot;, ..."]
    C -.-> N2["Each token → vector"]
    D -.-> N3["Add position info"]

    subgraph T["🔁 Transformer Block<br/>(Repeated N times)"]
        F["🧠 Multi-Head<br/>Self-Attention"] --> G["➕ Add & Normalize"]
        G --> H["⚙️ Feedforward Layer"]
        H --> I["➕ Add & Normalize"]
    end

    T --> O["📊 Output Embeddings<br/>(rich contextual vectors)"]

    classDef input fill:#E3F2FD,stroke:#1565C0,stroke-width:2px,color:#000;
    classDef token fill:#E8F5E9,stroke:#2E7D32,stroke-width:2px,color:#000;
    classDef embed fill:#FFF3E0,stroke:#EF6C00,stroke-width:2px,color:#000;
    classDef position fill:#E1F5FE,stroke:#0277BD,stroke-width:2px,color:#000;
    classDef transformer fill:#F3E5F5,stroke:#6A1B9A,stroke-width:3px,color:#000;
    classDef attention fill:#EDE7F6,stroke:#673AB7,stroke-width:2px,color:#000;
    classDef normalize fill:#FCE4EC,stroke:#C2185B,stroke-width:2px,color:#000;
    classDef feedforward fill:#FFF8E1,stroke:#F9A825,stroke-width:2px,color:#000;
    classDef note fill:#FAFAFA,stroke:#757575,stroke-width:1.5px,stroke-dasharray: 5 5,color:#000;
    classDef output fill:#E8F5E9,stroke:#1B5E20,stroke-width:3px,color:#000;

    class A input;
    class B token;
    class C embed;
    class D position;
    class T transformer;
    class F attention;
    class G,I normalize;
    class H feedforward;
    class N1,N2,N3 note;
    class O output;
```




https://poloclub.github.io/transformer-explainer/
https://www.youtube.com/watch?v=aircAruvnKk&list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi
```
