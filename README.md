# analyzeseo

analyzeseo is a library for analyzing website SEO (Search Engine Optimization), helping identify common issues and suggesting improvements to boost your site's search engine ranking.

## Installation

To install the library, you can use npm:

```bash
npm install analyzeseo
```
-----

### Usage
You can use the library to analyze a website by calling the `analyzeseo` function and passing the URL of the site to be analyzed. 

```js
const analyzeseo = require('analyzeseo');

analyzeseo('https://fasthost.cheap/') // Example
  .then(report => console.log(report))
  .catch(error => console.error(error));
```

### Example
When you call the analyzeseo function and pass a url you will get a report like this:

```js
{
  "title": "title is good",
  "description": "meta description is missing",
  "headings": "multiple H1 tags found there should be only one h1 tag per page",
  "images": "all images have alt attributes"
}
```

### Report Explanation
title: Checks for the presence and quality of the page title.

"title is good" means the title is present and looks good.
"title is missing" means the title is missing.
"title is too long/short" indicates the title is too long or too short.
description: Checks for the presence of the meta description.

"meta description is good" means the description is present and good.
"meta description is missing" means the description is missing.
headings: Checks the usage of heading tags.

"headings are good" means the heading usage is good.
"multiple H1 tags found there should be only one h1 tag per page" means there are multiple H1 tags, and there should be only one H1 tag per page.
images: Checks for the presence of alt attributes in images.

"all images have alt attributes" means all images have alt attributes.
"some images are missing alt attributes" means some images are missing alt attributes.