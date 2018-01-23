title: 主流浏览器及其内核
---

{%只是简单的说明一下，不做详细介绍%}

主流浏览器有:

``` bash
IE  Chrome  Firefox   Safari   Opera 
```


### Layout

这几个只是我个人觉得所占市场份额较大的浏览器.

浏览器 | 内核
--- | ---
`IE` | `Trident`
`Chrome` | `webkit/blink`
`Firefox` | `Gecko`
`Safari` | `webkit`
`Opera` | `Presto`

{% IE浏览器是微软开发的，所使用的内核为trident，其实绝大多数浏览器没有自己独立开发的内核，如360浏览器（使用trident，在其他版本也使用了webkit或blink），uc浏览器（使用blink和trident内核），其他的可以自己上网百度 %}
{% endnote %}

### Filename

By default, Hexo uses the post title as its filename. You can edit the `new_post_name` setting in `_config.yml` to change the default filename. For example, `:year-:month-:day-:title.md` will prefix filenames with the post creation date. You can use the following placeholders:

Placeholder | Description
--- | ---
`:title` | Post title (lower case, with spaces replaced by hyphens)
`:year` | Created year, e.g. `2015`
`:month` | Created month (leading zeros), e.g. `04`
`:i_month` | Created month (no leading zeros), e.g. `4`
`:day` | Created day (leading zeros), e.g. `07`
`:i_day` | Created day (no leading zeros), e.g. `7`

### Drafts

Previously, we mentioned a special layout in Hexo: `draft`. Posts initialized with this layout are saved to the `source/_drafts` folder. You can use the `publish` command to move drafts to the `source/_posts` folder. `publish` works in a similar way to the `new` command.

``` bash
$ hexo publish [layout] <title>
```

Drafts are not displayed by default. You can add the `--draft` option when running Hexo or enable the `render_drafts` setting in `_config.yml` to render drafts.

### Scaffolds

When creating posts, Hexo will build files based on the corresponding file in `scaffolds` folder. For example:

``` bash
$ hexo new photo "My Gallery"
```

When you run this command, Hexo will try to find `photo.md` in the `scaffolds` folder and build the post based on it. The following placeholders are available in scaffolds:

Placeholder | Description
--- | ---
`layout` | Layout
`title` | Title
`date` | File created date
