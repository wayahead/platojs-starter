# Project Plato

Plato project is the cornerstone for the SaaS platform, which is implemented on top of Next.js 14, and for the indie hacks.

## Initialize Project

### Create NextJS Project

```sh
$ npx create-next-app@14 plato --ts --tailwind --eslint --app --use-npm --yes
$ cd plato
$ vi tsconfig.json
{
  "compilerOptions": {...},
  "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", ".next/types/**/*.ts", "postcss.config.mjs"],
  "exclude": ["node_modules"]
}
```

### Install and Configure `autoprefixer`

```sh
$ npm install -D autoprefixer
$ vi postcss.config.mjs
vi postcss.config.mjs
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  }
}
```

### Create/Setup `shadcn`

```sh
$ npx shadcn@latest init -d
```

## Troubleshooting

### `Unknown rule at @tailwind` in `global.css`

1. install TailwindCSS plugin in VSCode.
2. add `Files: Associations` in VSCode settings with Item: *.css -> Value: tailwindcss