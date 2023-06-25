# Deploying a React App to GitHub Pages


Assuming you already have the **reactjs** or **nextjs** project completed.
Now let's deploy to git pages.

#

1. Install the **gh-pages** npm package

    Install the gh-pages npm package and designate it as a development dependency:

```cmd
$ npm install gh-pages --save-dev
```

At this point, the **gh-pages** npm package is installed on your computer and the React app's dependence upon it is documented in the React app's **package.json** file.

2. Add a **homepage** property to the **package.json** file
- Add a **homepage** property in this format: https://{username}.github.io/{repo-name}

```json
{
  "name": "my-app",
  "version": "0.1.0",
+ "homepage": "https://aniceto-jolela.github.io/bookstore",
  "private": true,
}
```

3. Add deployment scripts to the **package.json** file
-Add a **predeploy** property and a **deploy** property to the scripts object:

```json
"scripts": {
+   "predeploy": "npm run build",
+   "deploy": "gh-pages -d build",
    "start": "react-scripts start",
    "build": "react-scripts build",
}
```

```cmd
git add .
git commit -m "setup gh-pages"
git push
```

4. Push the React app to the GitHub repository

- Push the React app to the GitHub repository

```cmd
$ npm run deploy
```

![gh-pages](<assets/Captura de tela de 2023-06-25 16-46-41.png>)

### Autor : Aniceto Jolela 🥰
- [Linkedin](https://www.linkedin.com/in/aniceto-jolela-076547184/)