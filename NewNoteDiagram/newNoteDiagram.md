``` mermaid
sequenceDiagram
    participant user
    participant browser
    participant server

    user ->> browser: Open link
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate server
    server -->> browser: Display the requested page
    deactivate server

    user ->> browser: Enter the note and click Save button
    browser ->> server: POST notes with note data
    activate server
    server -->> browser: Data saved
    deactivate server


    

