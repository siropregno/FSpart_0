sequenceDiagram

participant browser
participant server

browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note

activate server
server-->>browser: note send to the server
deactivate server


browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes

activate server
server-->>browser: HTML file
deactivate server


browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css

activate server
server-->>browser: CSS file
deactivate server


browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js

activate server
server-->>browser: JS file
deactivate server


browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json

activate server
server-->>browser: JSON file with the new note
deactivate server