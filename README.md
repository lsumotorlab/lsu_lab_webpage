# LSU Skill Acquisition Lab Website

This is the source code for the LSU Skill Acquisition Lab website, built with Quarto.

## Prerequisites

- [Quarto](https://quarto.org/docs/get-started/) installed on your computer
- (Optional) RStudio if you prefer working in an IDE
- Git for version control
- GitHub account for hosting (if using GitHub Pages)

## Local Development

### Preview the website locally:

```bash
quarto preview
```

This will open a browser window with a live preview. Changes you make to the .qmd files will automatically update.

### Build the website:

```bash
quarto render
```

This generates the HTML files in the `docs/` folder.

## Customization

### Adding Content

1. **Team Members**: Edit `team.qmd` to add bios for each team member
2. **Publications**: Edit `publications.qmd` to add your publications organized by year
3. **Gallery**: 
   - Create an `images/` folder in the project directory
   - Add your photos to this folder
   - Edit `gallery.qmd` to replace placeholder images with your actual images
4. **Update Links**: Add your Google Scholar, ResearchGate, and ORCID links in `publications.qmd`

### Changing Colors/Style

Edit `custom.scss` to change the color scheme:
- `$primary`: Main blue color (currently #1e3a8a)
- `$secondary`: Secondary gray color
- `$link-color`: Link color

## Deployment to GitHub Pages

### Option 1: Automatic with GitHub Actions

1. Create a new repository on GitHub
2. Push your code:
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/lsu-skill-lab.git
git push -u origin main
```

3. In your repository settings:
   - Go to Settings → Pages
   - Source: Deploy from a branch
   - Branch: main, folder: /docs
   - Save

4. Update the `site-url` in `_quarto.yml` to match your GitHub Pages URL

### Option 2: Manual Deployment

1. Run `quarto render` locally
2. The `docs/` folder contains your website
3. Push to GitHub and configure Pages to serve from the `docs/` folder

## File Structure

```
lsu-skill-lab/
├── _quarto.yml          # Main configuration
├── custom.scss          # Custom SCSS theme
├── styles.css           # Additional CSS styles
├── index.qmd           # Home page
├── team.qmd            # Team page
├── publications.qmd     # Publications page
├── gallery.qmd         # Gallery page
├── contact.qmd         # Contact page
├── join.qmd            # Join Us page
├── images/             # (create this folder for images)
└── docs/               # Generated website (created after render)
```

## Support

For Quarto documentation and support:
- [Quarto Website Guide](https://quarto.org/docs/websites/)
- [Quarto GitHub Discussions](https://github.com/quarto-dev/quarto-cli/discussions)

## License

© 2025 LSU Skill Acquisition Lab. All rights reserved.
