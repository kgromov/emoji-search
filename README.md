# Emoji Search

- SQLite (wasm)
- sqlite-vec (vector search)
- Transformers.js (embedder)
- EmbeddingGemma (encoder/decoder)


Few caveats regarding firebase emulator:
- In order to launch UI it's required to specify project_id: 
```shell
!  emulators: The Emulator UI is not starting, either because none of the running emulators have a UI component \
or the Emulator UI cannot determine the Project ID. Pass the --project flag to specify a project.
```
E.g.:
``firebase emulators:start --only firestore --project 'demo-no-project'
``
`projectId` can be found in firebase configuration:
```typescript
const app = initializeApp({
    projectId: 'demo-no-project'
});
```
- After executed command above emulator is stared by default on port `3131` and ui is available at   
`http://127.0.0.1:4000/firestore`