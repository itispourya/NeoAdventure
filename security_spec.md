# Security Spec
## Data Invariants
1. `savedLocations` must belong to the user authenticating the request.
2. The user can only create, update or delete their own saved locations.
3. `userId` must equal `request.auth.uid`.

## Dirty Dozen Payloads
- Create without auth
- Create with mismatched userId
- Update modifying userId
- Read someone else's location
