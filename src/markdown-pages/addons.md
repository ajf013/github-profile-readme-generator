---
slug: "/addons"
date: "2021-06-01"
title: "🚀 Addons"
---

GitHub Profile README Generator tool uses few open-source addons developed by other developers. Including such features makes the tool useful. The developers of this tool is very grateful to use these awesome addons.

## [GitHub README Stats](https://github.com/anuraghazra/github-readme-stats)

⚡️ Dynamically generated stats for your github readmes

#### GitHub Stats Card

<a href="https://github.com/ajf013" target="blank">
  <img src="https://github-readme-stats.vercel.app/api?username=ajf013&show_icons=true" width="320" alt="AJF013's github stats"/>
</a>

#### Top Skills Card

<a href="https://github.com/ajf013" target="blank">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ajf013&layout=compact&hide=html" width="320" alt="ajf013's github top skills"/>
</a>

Developed by [Anurag Hazra](https://github.com/anuraghazra).

You can customize the theme too. See how to customize yours [here](https://github.com/anuraghazra/github-readme-stats)

<br/>

## [GitHub Readme Streak Stats](https://github.com/DenverCoder1/github-readme-streak-stats)

Stay motivated while contributing to open source by displaying your current contribution streak

![ajf013](https://github-readme-streak-stats.herokuapp.com/?user=ajf013)

Developed by by [Jonah Lawrence](https://github.com/DenverCoder1).

See how to customize the theme [here](https://github.com/DenverCoder1/github-readme-streak-stats)

<br/>

## [GitHub Profile Views Counter](https://github.com/antonkomarev/github-profile-views-counter)

It counts how many times your GitHub profile has been viewed. Free cloud micro-service.

![ajf013](https://komarev.com/ghpvc/?username=ajf013&style=flat-square)

Developed by by [Anton Komarev](https://github.com/antonkomarev).

You can customize the color, label and style too. See how to customize [here](https://github.com/antonkomarev/github-profile-views-counter)

<br/>

## [Dynamic Latest Blog Posts](https://github.com/gautamkrishnar/blog-post-workflow)

Show your latest blog posts from any sources(like dev(.)to, medium etc) or StackOverflow activity on your GitHub profile/project readme automatically using the RSS feed.

<img src="https://user-images.githubusercontent.com/8397274/88047382-29b8b280-cb6f-11ea-9efb-2af2b10f3e0c.png" width="320" alt="dynamic latest blog example"/>

Developed by [Gautam Krishna R](https://github.com/gautamkrishnar)

### How to use

- Go to your repository
- Add the following section to your **README.md** file, you can give whatever title you want. Just make sure that you use **<!-- BLOG-POST-LIST:START --><!-- BLOG-POST-LIST:END -->** in your readme. The workflow will replace this comment with the actual blog post list:

```markdown
# Blog posts

<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->
```

- Create a folder named `.github` and create `workflows` folder inside it if it doesn't exist.
- Create a new file named `blog-post-workflow.yml` with the following contents inside the workflows folder:

```yaml
name: Latest blog post workflow
on:
  schedule:
    # Runs every hour
    - cron: "0 * * * *"
jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://ajf013.blogspot.com, "
```

- Replace the above url list with your own rss feed urls. See [popular-sources](#popular-sources) for a list of common RSS feed urls.
- Commit and wait for it to run

To know more, check out the [official github repository](https://github.com/gautamkrishnar/blog-post-workflow)
