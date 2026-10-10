# palaeophidia.github.io

Personal academic website for Andrés Alfonso-Rojas, built with Jekyll and hosted on GitHub Pages.

---

## First-time setup

### 1. Create the GitHub repository

1. Go to [github.com](https://github.com) and sign in to the **palaeophidia** account.
2. Create a new repository named exactly **`palaeophidia.github.io`**.
3. Leave it empty (no README, no .gitignore).

### 2. Upload your files

In your terminal, navigate to this folder and run:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/palaeophidia/palaeophidia.github.io.git
git push -u origin main
```

GitHub Pages will automatically build and publish the site. It usually goes live within a minute or two at **https://palaeophidia.github.io**.

### 3. Add your profile photo

Place a photo named `profile.jpg` (square crop works best, at least 200×200 px) at:

```
public/img/profile.jpg
```

Then commit and push:

```bash
git add public/img/profile.jpg
git commit -m "Add profile photo"
git push
```

### 4. Add your CV

Place your CV PDF at:

```
public/cv/Alfonso-Rojas_CV.pdf
```

Then commit and push:

```bash
git add public/cv/Alfonso-Rojas_CV.pdf
git commit -m "Add CV"
git push
```

---

## Adding snake photos

1. Add photos to `public/img/snakes/` (e.g., `anaconda.jpg`).
2. Edit `snakepics/index.md` — replace each placeholder block with a real `<img>`:

```html
<div class="snakepics-item">
  <img src="/public/img/snakes/anaconda.jpg" alt="Eunectes murinus">
  <p class="snakepics-caption"><em>Eunectes murinus</em> — Green anaconda, Colombia</p>
</div>
```

---

## Adding field work photos

1. Add photos to `public/img/fieldwork/`.
2. Edit `fieldwork/index.md` — replace each placeholder `<div class="fieldwork-card-img img-placeholder">` with:

```html
<img class="fieldwork-card-img" src="/public/img/fieldwork/laventa.jpg" alt="La Venta">
```

---

## Local preview (optional)

Requires Ruby ≥ 3.0 and Bundler:

```bash
bundle install
bundle exec jekyll serve
```

Then open [http://localhost:4000](http://localhost:4000).

---

## Adding a new publication

Open `publications/index.md` and add a new `<div class="pub-item">` block inside the appropriate year group (or create a new year group at the top).

```html
<div class="pub-year-group">
<p class="pub-year">2027</p>

<div class="pub-item">
  <p class="pub-authors"><strong>Alfonso-Rojas, A.</strong>, &amp; Collaborator, B.</p>
  <p><span class="pub-title">Title of the paper.</span> <span class="pub-journal"><em>Journal Name</em>, volume(issue), pages.</span></p>
</div>
</div>
```

To add a DOI link to the title, wrap the title text in an anchor:

```html
<span class="pub-title"><a href="https://doi.org/10.XXXX/xxxxx" target="_blank">Title of the paper.</a></span>
```
