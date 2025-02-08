# Flow Diagram for Scoreboard Service

```mermaid
graph TD;
    A[User Action] -->|Triggers API Call| B[API Endpoint];
    B -->|Validates User| C{Is User Authorized?};
    C -->|Yes| D[Update Score in Database];
    C -->|No| E[Return Unauthorized Response];
    D --> F[Emit Score Update Event];
    F --> G[Update Scoreboard in Real-Time];
    G --> H[Display Updated Scores on Website];
```

This diagram illustrates the flow of execution for the scoreboard service, showing how user actions lead to score updates while ensuring authorization checks are in place.