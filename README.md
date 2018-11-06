# redirect.risd.systems

A website to handle redirects from Firebase password reset forms.

Firebase password reset URLs include a `continuationURL`, which neesd to be a whitelisted domain. `redirect.risd.systems` has been whitelisted, and is ready to handle requests such as `https://redirect.risd.systems/index.html?to=https%253A%252F%252Fedu.risd.systems%252Fcms&lang=en`, which will redirect the browser to `https://edu.risd.systems/cms`.

This redirect URL usage is defined within the [`risd/webhook-cms`](https://github.com/risd/webhook-cms), where password reset emails are created. The usage pattern is as described above.


### development

`npm install` to get the development dependencies.

`npm start` to start the development server, a static file server to mimic the Google Cloud Storage site hosting environment that this is deployed to.

`npm run deploy` will push the `public/` directory to `redirect.risd.systems`.
