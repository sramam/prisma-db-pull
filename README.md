## Reproduce

```
git clone https://github.com/sramam/prisma-db-pull.git 
cd prisma-db-pull
npm install
npx prisma db pull
```

## Trouble with `npx prisma db pull`

```
❯ npx prisma db pull
Prisma schema loaded from prisma/schema.prisma
Environment variables loaded from .env
Datasource "db": MySQL database
Error: Prisma schema validation - (get-config wasm)
Error code: P1012
error: Error validating datasource `db`: the URL must start with the protocol `mysql://`.
  -->  schema.prisma:6
   | 
 5 |   provider = "mysql"
 6 |   url      = env("DATABASE_URL")
   | 

Validation Error Count: 1
[Context: getConfig]

Prisma CLI Version : 4.9.0
```

### versions

```
❯ prisma -v
zsh: command not found: prisma
❯ npx prisma --version
Environment variables loaded from .env
prisma                  : 4.9.0
@prisma/client          : Not found
Current platform        : darwin-arm64
Query Engine (Node-API) : libquery-engine ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5 (at node_modules/@prisma/engines/libquery_engine-darwin-arm64.dylib.node)
Migration Engine        : migration-engine-cli ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5 (at node_modules/@prisma/engines/migration-engine-darwin-arm64)
Introspection Engine    : introspection-core ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5 (at node_modules/@prisma/engines/introspection-engine-darwin-arm64)
Format Binary           : prisma-fmt ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5 (at node_modules/@prisma/engines/prisma-fmt-darwin-arm64)
Format Wasm             : @prisma/prisma-fmt-wasm 4.9.0-42.ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5
Default Engines Hash    : ceb5c99003b99c9ee2c1d2e618e359c14aef2ea5
Studio                  : 0.479.0
❯ node -v
v18.13.0
❯ npm -v
8.19.3
```