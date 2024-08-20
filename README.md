# GitHub pages deployment process for Vite-based React apps (frontend only)

**1. Install gh-pages Package**
```
npm install gh-pages --save-dev
```

**2. Update vite.config.js**
```
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  base: '/your-repo/',  // Update this line
});
```

**3. Update package.json**
```
"homepage": "https://your-username.github.io/your-repo",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d dist"
}
```

**4. Build and Deploy**
```
npm run deploy
```

**5. Set GitHub Pages Source**
- Go to your repository on GitHub, click on **Settings > Pages**, and ensure the source is set to the **gh-pages** branch.

**6. Access Your Deployed Site**
- Your Vite-based React app should now be live on GitHub Pages at **https://your-username.github.io/your-repo**.
