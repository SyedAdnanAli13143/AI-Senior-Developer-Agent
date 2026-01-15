flowchart TB
    Start([Start])

    Start --> TaskInput["Product / Feature Request"]

    TaskInput --> Orchestrator

    subgraph Orchestrator["AI Senior Developer Agent (Orchestrator)"]
        direction TB

        AgentStart(("[Agent Execution Begins]"))

        AgentStart --> RequirementAnalysis
        RequirementAnalysis["Requirement Analysis<br/>(Understand scope & constraints)"]

        RequirementAnalysis --> ArchitectureDesign
        ArchitectureDesign["System Architecture & Tech Decisions"]

        ArchitectureDesign --> DevLoop{"Development Tasks"}

        subgraph FrontendService["Frontend Development Service"]
            FE["Angular Development<br/>(Components, Services, UI)"]
        end

        subgraph BackendService["Backend Development Service"]
            BE["Django REST API Development<br/>(Models, APIs, Auth)"]
        end

        subgraph DatabaseService["Database Design Service"]
            DBDesign["PostgreSQL Schema & Migrations"]
        end

        DevLoop --> |"Frontend Tasks"| FE
        DevLoop --> |"Backend Tasks"| BE
        BE --> DBDesign

        FE --> Review
        BE --> Review

        subgraph ReviewService["Senior Code Review Service"]
            Review["Code Review & Refactoring"]
            Review --> Testing["Testing & Validation"]
        end

        Testing --> DeployStep

        subgraph DeploymentService["Deployment Service"]
            DeployStep["Dockerization & Environment Setup"]
            DeployStep --> Deployment["Production Deployment"]
        end

        Deployment --> AgentEnd(("[Agent Execution Complete]"))
    end

    Orchestrator --> Output["Production-Ready Full-Stack Application"]
    Output --> End([End])

    %% Styling
    style Orchestrator fill:#fffade,stroke:#d09d00,stroke-width:2px
    style FrontendService fill:#e1f5ff
    style BackendService fill:#e1f5ff
    style DatabaseService fill:#e8f5e9
    style ReviewService fill:#f3f3f3
    style DeploymentService fill:#f7e1ff
