# NODE: API CON POSTGRES JWT Y TS

- node 20.11.1

## INSTALANDO DEPENDENCIAS

```bash
npm i ts-node-dev @types/express @types/jsonwebtoken @types/bcrypt @types/node rimraf prisma --save-dev 
npm i express jsonwebtoken bcrypt @prisma/client dotenv typescript 
```

## CONFIGURAR TYPESCRIPT

```bash
npx tsc --init --outDir dist/ --rootDir src
```

### MODIFICAR tsconfig.json

```json
{
    ...
    "exclude": [
        "node_modules", "dist"
    ]
    "include": [
        "src"
    ]
    ...
    "compilerOptions": {
    ...
}
```

## MODIFICAR package.json: SCRIPTS

```json
{
    ...
    "scripts" : {
        "dev": "tsnd --respawn --clear src/server.ts"
    }
}
```

## CREAR ARBOL DIRECTORIOS PROYECTO

```text
./
    .env
    src/
        app.ts
    server/
        server.ts
    routes/
        authRoutes.ts
    controllers
```
