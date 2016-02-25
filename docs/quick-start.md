In order for Enfield to know how to build your site you'll need to specify a `.yml` config file.

Your config can be called whatever you like. The default that Enfield will look like is `config.yml` in the root of your project.

You will also need a theme. You can [download a sample theme from github](TODO) to get going for now and paste it into your project.

Additionally you'll need some markdown files. These too can be anywhere you like.

Assuming your folder looks like:
```yaml
- docs/
    - home.md
    - dogs.md
    - cats.md
    - hamsters.md
    - bunnies.md
- theme/
- config.yml
```

You'll need to specify the structure of your site in your `config.yaml` like so:
```yaml
title: 'enfield'
theme: 'theme/'
pages:
    - Why You Need A Pet: 'docs/home.md'
    - Mammals:
        - How Dogs Work: 'docs/dogs.md'
        - How To Setup a Cat: 'docs/cats.md'
    - Other Animals:
        - Hamsters: 'docs/hamsters.md'
        - Bunnies: 'docs/bunnies.md'
```
For each page you have to specify the location of the markdown file that corresponds to that page.

If you want to break up your pages in sections you can just nest a list of pages like above.

To see what it looks like, run:
```bash
$ enfield --serve --watch
```
This will watch for file changes and rebuild your site as you make changes.