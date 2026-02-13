## Local development (Jekyll)

This site uses Jekyll with Bundler and the gems defined in `Gemfile`.

### 1) Prerequisites

Install Ruby and build tools.

On Ubuntu/Debian:

```bash
sudo apt update
sudo apt install -y ruby-full build-essential zlib1g-dev
```

Install Bundler (if not already installed):

```bash
gem install bundler
```

### 2) Install project dependencies

From the repository root:

```bash
bundle install
```

### 3) Run the site locally

Serve the site:

```bash
bundle exec jekyll serve
```

Jekyll will build the site and host it locally at:

- <http://127.0.0.1:4000>
- <http://localhost:4000>

### 4) Optional useful flags

Enable live reload while editing:

```bash
bundle exec jekyll serve --livereload
```

Use a custom port:

```bash
bundle exec jekyll serve --port 8080
```

### 5) Build without serving

```bash
bundle exec jekyll build
```

Generated output goes to `_site/`.

### Troubleshooting

- If you see a `webrick` error, run `bundle install` again (the Gemfile already includes `webrick`).
- If port `4000` is busy, start with another port (for example `--port 8080`).
- If gems fail to install due to permissions, avoid `sudo bundle ...`; use a user-local Ruby setup or a version manager.
