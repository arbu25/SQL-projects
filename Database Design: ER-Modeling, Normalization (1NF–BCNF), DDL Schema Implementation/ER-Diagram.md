```mermaid
erDiagram
    ganre |--o{ executor : "id_ganre"
    ganre |--o{ albom : "id_ganre"
    ganre |--o{ composition : "id_ganre"
    executor |--o{ composition : "id_executor"
    albom |--o{ composition : "id_albom"

    ganre {
        integer id PK
        varchar name_ganre
    }

    albom {
        integer id PK
        varchar name_albom
        integer id_ganre FK
    }

    executor {
        integer id PK
        varchar full_name
        varchar type
        text description
        integer id_ganre FK
    }

    composition {
        integer id PK
        varchar name
        integer id_executor FK
        integer id_albom FK
        integer id_ganre FK
    }
```
