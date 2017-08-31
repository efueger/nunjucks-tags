[![Build Status](https://travis-ci.org/gaggle/nunchucks-tags.svg?branch=enable-travis)](https://travis-ci.org/gaggle/nunchucks-tags)
[![codecov](https://codecov.io/gh/gaggle/nunchucks-tags/branch/master/graph/badge.svg)](https://codecov.io/gh/gaggle/nunchucks-tags)
[![Known Vulnerabilities](https://snyk.io/test/github/gaggle/nunchucks-tags/badge.svg)](https://snyk.io/test/github/gaggle/nunchucks-tags)
[![Code Climate GPA](https://codeclimate.com/github/codeclimate/codeclimate/badges/gpa.svg)](https://codeclimate.com/github/codeclimate/codeclimate)

# Nunjucks tags
Wrapper around Nunjucks to make it easy to add custom tags like this:

```javascript
const NunjucksTags = require("nunjucks-tags")

const nunjucks = new NunjucksTags()

nunjucks.register("tag", (args) => args.join("/"))

nunjucks.render("{% tag Foo Bar %}")
  .then(res => console.log(res))
> Foo/Bar
```

# Development
Just run `npm test` and make sure to add tests 
![Graph of coverage/commits](https://codecov.io/gh/gaggle/nunchucks-tags/branch/master/graphs/commits.svg)

## Credits
Lifted from the excellent [Hexo] project by [Tommy Chen].

[Hexo]: https://hexo.io
[Tommy Chen]: https://github.com/tommy351
