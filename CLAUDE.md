# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Tech Stack

- **Ruby 2.7.0** / **Rails 6.0.6**
- **SQLite3** (all environments)
- **Webpacker** for JavaScript bundling, **Sprockets** for CSS/assets
- **Turbolinks**, **ActionCable**, **ActiveStorage** configured but minimal
- **Minitest** with Capybara/Selenium for system tests

## Common Commands

```bash
bin/setup                  # First-time setup (install gems, prepare DB, clear tmp)
bin/rails server           # Start dev server on port 3000
bin/rails console          # Rails REPL
bin/rails test             # Run all tests
bin/rails test test/models/foo_test.rb  # Run a single test file
bin/rails test test/models/foo_test.rb:42  # Run a single test by line number
bin/rails db:migrate       # Run pending migrations
bin/rails routes           # List all routes
```

## Architecture

This is a freshly initialized Rails 6 app with standard MVC structure. The project is in early development — no custom models, controllers, views, or routes exist yet beyond the Rails skeleton.

Notable: `config/boot.rb` has an added `require 'logger'` before Bundler setup to address a concurrent-ruby compatibility issue with Ruby 2.7.
