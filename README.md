# Astro + Tailwind CSS

## 🚀 Project Structure

Inside of your Astro project, you'll see the following folders and files:

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │    └── index.astro
│   ├── components/
│   │    
│   ├── styles/
│   │    └── global.css
│   └── assets/
└── package.json
```

To learn more about the folder structure of an Astro project, refer to [our guide on project structure](https://docs.astro.build/en/basics/project-structure/).

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `yarn install`            | Installs dependencies using Yarn                 |
| `yarn dev`                | Starts local dev server at `localhost:4321` using Yarn |
| `yarn build`              | Build your production site to `./dist/` using Yarn |
| `yarn preview`            | Preview your build locally, before deploying using Yarn |
| `yarn astro ...`          | Run CLI commands like `astro add`, `astro check` using Yarn |
| `yarn astro --help`       | Get help using the Astro CLI using Yarn          |

## 👀 Want to learn more?

Feel free to check [our documentation](https://docs.astro.build) or jump into our [Discord server](https://astro.build/chat).

## 📦 Using TailwindCSS

To add TailwindCSS to your Astro project, follow these steps:

1. Install TailwindCSS and its peer dependencies:

    ```sh
    yarn add @tailwindcss/vite
    ```

2. Configure Vite Plugin

    ```astro.config.mjs
    import { defineConfig } from "astro/config";
    import tailwindcss from "@tailwindcss/vite";
    // https://astro.build/config
    export default defineConfig({
    vite: {
        plugins: [tailwindcss()],
    },
    });
    
    ```

3. Add the following to your main CSS file (e.g., `src/styles/global.css`):

    ```css
    @import "tailwindcss";
    ```

4. Import the CSS file in your `src/pages/index.astro`:

    ```astro
    ---
    import '../styles/global.css';
    ---
    ```

Now you can use TailwindCSS classes in your Astro components.
