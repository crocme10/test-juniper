## Reproducing an error with juniper / warp

### Building

cargo build --release

### Testing

In one terminal window run the server:

```
RUST_LOG=debug ./target/release/test-juniper
```

Verify server is available with graphiql: Open a web browser and open
http://localhost:8080/graphiql

In another window, test `graphql` interface:

```
curl -X POST "http://localhost:8080/graphql" -H 'Content-Type: application/json' --data-binary @payload.json
Request body consumed multiple times
```
