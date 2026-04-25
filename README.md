# kevalmalde.github.io

Personal site for **Keval Malde**, built with [Jekyll](https://jekyllrb.com/) and the [Minima](https://github.com/jekyll/minima) theme, compatible with the [`github-pages`](https://github.com/github/pages-gem) gem (same stack [GitHub Pages](https://docs.github.com/en/pages) uses for Jekyll).

Live site: [https://kevalmalde.github.io](https://kevalmalde.github.io)

## Local development

**Requirements:** Ruby, Bundler (see [Ruby download](https://rubyinstaller.org/) on Windows, or your OS package manager).

```bash
bundle install
bundle exec jekyll serve
```

Open [http://127.0.0.1:4000](http://127.0.0.1:4000). On Ruby 3+, the `webrick` gem in the `Gemfile` helps `jekyll serve` work.

**Without Ruby installed:** you can build in Docker from the project root, for example:

```bash
docker run --rm -v "%cd%":/srv/jekyll -w /srv/jekyll jekyll/jekyll:4.2.2 sh -c "bundle install && bundle exec jekyll build"
```

(PowerShell: use `${PWD}` or the full path instead of `%cd%` if needed.)

## GitHub: repository and Pages

1. Create a **public** repository named **`kevalMalde.github.io`** (must match your GitHub username for a [user/organization site](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#types-of-github-pages-sites)).
2. Push this project’s `main` branch to that repository (include `Gemfile` and `Gemfile.lock` for reproducible local installs).
3. In the repo, go to **Settings → Pages** (or **Settings → Build and deployment**), set **Source** to **Deploy from a branch**, choose branch **`main`** and folder **`/ (root)`**.
4. After the first build finishes, the site is available at **https://kevalmalde.github.io** (can take a minute or two).

If a build fails, check the **Actions** or **Settings → Pages** build log. Typical issues: invalid YAML in `_config.yml`, or a plugin that is not in the [GitHub Pages allowlist](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll#plugins).

## Custom profile photo (optional)

The home page uses the [IITH lab image URL](https://newslab.iith.ac.in/images/people/mtech/keval.jpg) by default. To use a file in this repo instead, add (for example) `assets/images/profile.jpg` and change the `img` `src` in `index.md` to `/assets/images/profile.jpg`.
