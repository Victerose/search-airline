# py-web-search

[![Latest Version](https://pypip.in/version/py-web-search/badge.svg)](https://pypi.python.org/pypi/py-web-search/)

A Python module to fetch and parse results from different search engines.

### Table of Contents

* [Support](#search-engines-supported)
* [Installation](#installation)
* [Usage](#usage)
* [Todo](#todo)

## Search engines supported

* Google: web
* Bing: news, web

## Installation

Current release: 0.1.1.3

Needs Python3.
Install using pip: `pip install py-web-search`

## Usage

```python
    from pws.google import Google
    from pws.bing import Bing

    print(Google.search('hello world', 5, 2))
    print(Bing.search('hello world', 5, 2))
```
Prints 5 results from the the third result onwards (ignores the first 2) in the following format.

```
    {
        'url': '...',
        'num': 5,
        'start': 2,
        'search_engine': 'google',
        'results':
        [
            {
                'link': '...',
                'link_text': '...',
                'link_info': '...',
                'additional_links':
                {
                    linktext: link,
                    ...
                }
        	},
        	...
        ]
    }
```

## Todo

* Other search engines
* Images etc.