---
layout: post
title:  "Github Pages"
date:   2023-05-03 12:03:49 -0700
tags: note tool util
---

- [GitHub Pages](https://docs.github.com/en/pages):
    - Quickstart:
        - 1: New repository
        - 2: `username.github.io`
        - 3: repo > `Settings`
        - 4: `Code and automation` > `Pages`
        - 5: `Build and deployment` > `Source` > `Deploy from a branch`
        - 6: `Build and deployment` > `Branch` > branch (main)
        - 7: `README.md`
        - 8: Go to `username.github.io`
    - Get started
    - Setup site with Jekyll:
        - Overview:
            - Configuration:
                - `_config.yml`
        - Create github pages with jekyll:
            - Create repository: `username.github.io`
            - cd repo
            - `jekyll new --skip-bundle .`
            - `Gemfile` > comment out `gem "jekyll"`
            - `Gemfile` > change to `gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins`
            - `bundle install`
            - Push: |
                ---
                git init
                git remote add origin <url.git>
                git add .
                git commit -m "Initial GitHub pages site with Jekyll"
                git push -u origin main
                ---
            - `Settings` > `Code and automation` > `Pages`
            - Go to `username.github.io`
        - Test locally:
            - cd repo
            - bundle install
            - bundle exec jekyll serve
            - go to `localhost:4000`