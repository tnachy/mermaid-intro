# Introduction to Mermaid Diagrams

Mermaid is a JavaScript-based diagramming and charting tool that renders Markdown-inspired text definitions to create and modify diagrams dynamically. It is a powerful tool for creating UML diagrams directly within Markdown files.

## Supported UML Diagrams

### 1. Flowchart
```mermaid
%%{init: {'look': 'handDrawn'}}%%
graph TD
    A[Start] --> B{Is it?}
    B -->|Yes| C[OK]
    B -->|No| D[Not OK]
```

### 2. Sequence Diagram
```mermaid
%%{init: {'theme': 'forest'}}%%
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!    
```

### 3. Class Diagram
```mermaid
classDiagram
    class Animal {
      +String name
      +int age
      +void eat()
      +void sleep()
    }
    class Dog {
      +String breed
      +void bark()
    }
    Animal <|-- Dog
```

### 4. State Diagram
```mermaid
stateDiagram
    [*] --> Still
    Still --> [*]
    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

### 5. Entity Relationship Diagram
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER {
      string name
      string address
    }
    ORDER {
      int orderNumber
      date orderDate
    }
    LINE-ITEM {
      int quantity
      double price
    }
```

### 6. Gantt Chart
```mermaid
gantt
    title A Gantt Diagram
    dateFormat  YYYY-MM-DD
    section Section
    A task           :a1, 2023-01-01, 30d
    Another task     :after a1  , 20d
    section Another
    Task in sec      :2023-02-01  , 12d
    another task     : 24d
```

### 7. Pie Chart
```mermaid
pie
    title Key Elements
    "Element A" : 40
    "Element B" : 30
    "Element C" : 20
    "Element D" : 10
```
### 8. XY Chart
```mermaid
xychart-beta
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
    line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
```

### 9. Journey Diagram
```mermaid
journey
    title My Working Day
    section Go to Work
      Make coffee: 5: Me
      Go to work: 1: Me
    section Work
      Code: 3: Me
      Meeting: 2: Me
      Review: 2: Me
    section Go home
      Relax: 5: Me
```
Mermaid provides a versatile way to create various types of diagrams using simple text syntax. For more details, visit the [Mermaid documentation](https://mermaid-js.github.io/mermaid/#/).