# ai-platform-demo


## Deployment on Vercel

1. Do **NOT** commit real keys. Use the `js/env.example.js` as a template.
2. Create `js/env.js` on the server (or in Vercel build) with real values:

```js
window.__env = {
  SUPABASE_URL: "https://your-project.supabase.co",
  SUPABASE_ANON_KEY: "your-anon-key"
};
```

3. Add `env.js` to `.gitignore`.
4. Configure Vercel project (Environment Variables) or add a build step to generate `js/env.js` from Vercel env vars.

Example build script in package.json (optional):

```json
"scripts":{
  "build:env": "node scripts/generate-env.js"
}
```

Or add a simple server-side script to write `js/env.js` during deployment.
