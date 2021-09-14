# Steps to reproduce

```
npx @docusaurus/init@latest init my-website classic
```

Was version beta.6 at time of writing

Then edit docs/intro to have a section header, and link to a couple other pages

Then run

```
yarn build
cd build
python3 -m http.server
```

This starts on http://localhost:8000

Visit http://localhost:8000/docs/intro#section-heading

The URL is automatically rewritten (chrome 93, firefox 92) to http://localhost:8000/docs/intro/#section-heading

Then click a ex1 link, goes to non-existent page 404

http://localhost:8000/docs/intro/ex1
