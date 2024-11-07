# Tailwind CSS CLI Setup

This project is set up to use Tailwind CSS via the CLI. Follow these steps to install the dependencies, configure Tailwind, and start using it in your project.

---

## Getting Started

1. **Initialize the Project**

   Run the following command to create a `package.json` file, which will manage your project’s dependencies:

   ```bash
   npm init

   ```

2. **Install Tailwind CSS**

   Install Tailwind CSS as a development dependency:

   ```bash
   npm install -D tailwindcss

   ```

3. **Initialize Tailwind CSS**

   Use this command to generate a `tailwind.config.js` file, where you can customize Tailwind’s configuration:

   ```bash
   npx tailwindcss init

   ```

4. **Configure Tailwind Content Paths**

   In `tailwind.config.js`, specify the content files Tailwind should scan to generate styles:

   ```bash
   content: ["./*.html"],

   This tells Tailwind where to look for HTML files, ensuring it only generates the CSS needed for these files.

   ```

5. **Setup Scripts in `package.json`**

   Add the following lines to the scripts section in `package.json`:

   ```bash
   "scripts": {
     "build": "tailwindcss -i ./input.css -o styles/style.css",
     "watch": "tailwindcss -i ./input.css -o styles/style.css --watch"
   }

   *build: Compiles Tailwind styles into `styles/style.css`.
   *watch: Automatically rebuilds the CSS whenever there are changes to the input files.

   ```

6. **Create Input CSS File**

   In `input.css`, add these Tailwind directives:

   ```bash
   @tailwind base;
   @tailwind components;
   @tailwind utilities;

   These directives include Tailwind's base, component, and utility styles, which are essential for using Tailwind’s classes.

   ```

7. **Run Tailwind Watch Mode**

   Start Tailwind in watch mode with the following command:

   ```bash
   npm run watch

   This will create a styles folder containing the compiled style.css file. The file will automatically update each time you make changes to `input.css`.

   ```

8. **Link To Use**

   ```bash
   <link href="styles/style.css" rel="stylesheet">


   ***NB:*** Further if we want to create node modules folder then just run
   ```

```bash
npm i

this command will create that.
```
