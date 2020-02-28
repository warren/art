# Warren's Art

My art portfolio, hosted on GitHub Pages. https://art.warrenpartridge.me

It's a simple Jekyll site that uses Midzer's [Urban Theme](https://github.com/midzer/urban-theme).

## Branch Structure

* `master` is where all the work gets done.
* `gh-pages` is the live branch, where all the Jekyll-generated files go.

## Deploying

It's super easy if you use git worktree (and you totally should). I'll explain how to set that up in the next section.

Assuming you already have the working tree set up, you can deploy by doing:
1) `bundle exec jekyll build`
2) `cd _site`
3) `git commit`
4) `git push`

## Setup

You'll first need to download [Ruby](https://www.ruby-lang.org/en/downloads/).

You'll also need Bundler and Jekyll, so do `gem install bundler jekyll` to get those after installing Ruby.

That's it! You can now do `bundle exec jekyll serve` to run the blog locally or `bundle exec jekyll build` to generate the blog under `_site`.

<br>

If you want to set up git worktree for quick deploys: from the repository root, run

```git worktree add -B gh-pages _site origin/gh-pages```

This command signals to git that the `_site` directory (which is where Jekyll builds all of its files) should actually be the `gh-pages` branch's root directory. So, any files you build with Jekyll are automatically piped to the live branch - you just need to commit and push them and you're deployed!
