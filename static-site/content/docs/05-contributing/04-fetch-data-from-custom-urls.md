---
title: "Fetch Datasets accessible via your own URL"
---

We want to allow researchers the maximum amount of control over where their data lives and who controls it.
We promote a couple of easy-to-use methods to facilitating this - [Nextstrain Groups](./nextstrain-groups), where the data are stored on Amazon AWS S3 and [Nextstrain Community](./community-builds) where the data lives within your own GitHub repos. 
This page describes a third way:

**Datasets or narratives which are accessible via a public URL can be accessed through a `nextstrain.org/fetch/...` URL**

* Given an Auspice v2 dataset JSON available at publicly accessible URL `<URL>`, the dataset may be accessed via `https://nextstrain.org/fetch/<URL>`.
* Given a narrative markdown file  available at publicly accessible URL `<URL>`, the dataset may be accessed via `https://nextstrain.org/fetch/narratives/<URL>`.

Note that we recommend that the dataset is stored (or transmitted) compressed to improve loading times.
Currently sidecar files (such as frequencies) are not able to be loaded via this method.
Datasets which are not currently 
URL queries are currently ignored.


### Examples

1. **Single dataset** The nextstrain zika dataset is accessible at https://data.nextstrain.org/zika.json (click that link to see the actual JSON data)
and can therefore be viewed within nextstrain.org at https://nextstrain.org/fetch/https://data.nextstrain.org/zika.json.

2. **Narratives** There is an introductory narrative stored in our GitHub repo and therefore accessible via the URL https://raw.githubusercontent.com/nextstrain/narratives/master/intro-to-narratives.md (click there to read the actual markdown file).
You can see this rendered in Nextstrain at: https://nextstrain.org/fetch/https://raw.githubusercontent.com/nextstrain/narratives/master/intro-to-narratives.md.

3. **Dual trees** Displaying two trees side-by-side is possible using the same syntax as with other dataset sources, e.g. https://nextstrain.org/fetch/https://data.nextstrain.org/flu_seasonal_yam_na_2y.json:fetch/https://data.nextstrain.org/flu_seasonal_yam_ha_2y.json


### How do I manage the data storage?

That's completely up to you - all that we require for this to work is that it's publicly accessible via a URL. 
It could be a static asset (e.g. AWS S3) or a server which responds dynamically.
P.S. If you build something interesting here, for instance a server which generates the JSON on-the-fly, we'd love to [hear from you!](mailto:hello@nextstrain.org).
