# Git Workflow Diagram

```mermaid
gitGraph
    commit id: "Initial commit"
    branch develop
    checkout develop
    commit id: "Add feature files"
    commit id: "Update documentation"
    
    branch feature/user-auth
    checkout feature/user-auth
    commit id: "Add auth logic"
    commit id: "Fix auth bugs"
    
    checkout develop
    merge feature/user-auth
    commit id: "Merge auth feature"
    
    branch feature/ui-update
    checkout feature/ui-update
    commit id: "Update UI components"
    
    checkout develop
    merge feature/ui-update
    
    checkout main
    merge develop tag: "v1.0.0"
    
    commit id: "Hotfix production"
    checkout develop
    merge main
```

## Git Branching Strategy

This diagram illustrates a common Git workflow:

1. **Main Branch**: Production-ready code
2. **Develop Branch**: Integration branch for features
3. **Feature Branches**: Isolated development work
4. **Merges**: Integrating changes between branches
5. **Tags**: Version releases

The workflow shows how features are developed in isolation, merged to develop for integration, and finally released to production through main branch merges.
