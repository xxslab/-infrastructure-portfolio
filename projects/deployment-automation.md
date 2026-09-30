# Production Deployment & Operations Automation

## Goal
Replace ad-hoc production edits with a guarded, repeatable deployment process.

## Workflow
```mermaid
flowchart LR
    CHANGE[Candidate change] --> BASE[Baseline verification]
    BASE -->|unchanged| DRY[Dry run]
    BASE -->|drift detected| STOP[Abort]
    DRY --> BACKUP[Backup]
    BACKUP --> APPLY[Controlled apply]
    APPLY --> VERIFY[Verification]
    VERIFY -->|failure| ROLLBACK[Rollback]
    VERIFY -->|success| SYNC[Sync + document]
```

## Engineering principles
- detect production drift before applying changes
- create a recoverable state before modification
- make rollback explicit
- verify the actual served state after deployment
- keep operational documentation with version-controlled changes
- automate repetitive checks instead of relying on memory

## Technologies
Linux · Bash · Python · Git · Apache/Nginx · Plesk · DNS · TLS · deployment scripting · monitoring

## Skills demonstrated
production operations · change safety · troubleshooting · scripting · recovery design · documentation
