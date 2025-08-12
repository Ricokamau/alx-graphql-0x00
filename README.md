# ALX GraphQL - 0x00 Rick and Morty API Queries

## 📌 Description
This repository contains GraphQL queries and their outputs for retrieving data from the [Rick and Morty GraphQL API](https://rickandmortyapi.com/graphql).  
The tasks are split into two main directories:
- `character/` → Queries related to characters.
- `episode/` → Queries related to episodes.

The files in each directory follow a clear naming convention that pairs the `.graphql` query with its `.json` output.

---

## 📂 Repository Structure
alx-graphql-0x00/
│
├── character/
│ ├── character-id-1.graphql
│ ├── character-id-1-output.json
│ ├── character-id-2.graphql
│ ├── character-id-2-output.json
│ ├── character-id-3.graphql
│ ├── character-id-3-output.json
│ ├── character-id-4.graphql
│ ├── character-id-4-output.json
│ ├── characters-page-1.graphql
│ ├── characters-page-1-output.json
│ ├── characters-page-2.graphql
│ ├── characters-page-2-output.json
│ ├── characters-page-3.graphql
│ ├── characters-page-3-output.json
│ ├── characters-page-4.graphql
│ └── characters-page-4-output.json
│
├── episode/
│ ├── episode-id-1.graphql
│ ├── episode-id-1-output.json
│ ├── episode-id-2.graphql
│ ├── episode-id-2-output.json
│ ├── episode-id-3.graphql
│ ├── episode-id-3-output.json
│ ├── episode-id-4.graphql
│ └── episode-id-4-output.json
│
└── README.md

yaml
Copy
Edit

---

## 🛠️ Requirements
- [GraphQL Playground](https://rickandmortyapi.com/graphql) or any GraphQL client
- Internet connection to access the API

---

## 🚀 How to Run Queries

1. **Open the Rick and Morty GraphQL Playground**  
   Visit:  
https://rickandmortyapi.com/graphql

pgsql
Copy
Edit

2. **Copy a `.graphql` query** from either `character/` or `episode/`.

3. **Paste it into the Playground** and execute the query.

4. **Compare with the `.json` output** file in the repository to verify correctness.

---

## 📌 Example Query (Character by ID)
**File:** `character/character-id-1.graphql`
```graphql
query {
character(id: 1) {
 id
 name
 status
 species
 gender
 origin {
   name
 }
 location {
   name
 }
 image
}
}
📌 Example Output
File: character/character-id-1-output.json

json
Copy
Edit
{
  "data": {
    "character": {
      "id": "1",
      "name": "Rick Sanchez",
      "status": "Alive",
      "species": "Human",
      "gender": "Male",
      "origin": {
        "name": "Earth (C-137)"
      },
      "location": {
        "name": "Earth (Replacement Dimension)"
      },
      "image": "https://rickandmortyapi.com/api/character/avatar/1.jpeg"
    }
  }
}
🧾 Notes
The API uses a single endpoint for all queries.

Variables can be used for dynamic queries (e.g., $id: ID! for IDs).
