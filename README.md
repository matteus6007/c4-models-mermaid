# Building C4 Models using Mermaid

https://mermaid.js.org/syntax/c4.html

## Husky Githooks

https://typicode.github.io/husky/

```
npx husky-init && npm install
```

## Building Images

https://github.com/mermaid-js/mermaid-cli

### CLI

_NPM is already included in the `package.json`._ 

Generate diagram image:

```
./node_modules/.bin/mmdc -i ./diagrams/context.mmd -o ./diagrams/context.svg
```

Generate markdown with diagrams to `/docs` folder:

```
./node_modules/.bin/mmdc -i ./diagrams/diagrams.template.md -o ./docs/diagrams.md
```

### Docker

Install Docker image:

```
docker pull minlag/mermaid-cli
```

Generate diagram image:

```
docker run --rm -v $PWD/diagrams:/data minlag/mermaid-cli -i context.mmd -o context.svg
```

Generate markdown with diagrams to `/docs` folder:

```
docker run --rm -v $PWD/diagrams:/data -v $PWD/docs:/docs minlag/mermaid-cli -i diagrams.template.md -o /docs/diagrams.md
```