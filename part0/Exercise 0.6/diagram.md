# Exercise 0.6
New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: User creates a new note.

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    Note right of browser: New node sent via JSON File.

    server-->>browser: Status 201 - Node Created
    deactivate server

    Note right of browser: Event Handler renders the new node.