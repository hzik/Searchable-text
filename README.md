# Searchable text

With this custom element you can search by words in your Text elements.

## Setup

1. Deploy the code to a secure public host
    * See [deploying section](#Deploying) for a really quick option
2. Configure Custom element in Kontent.ai UI
    * The `Hosted code URL` is where you deployed to in step 1
    * `Allow the custom element to read values of specific elements` select the text you would like to index
    * `JSON parameters`:
```json
{
    "source_text": "codename_of_text_element"
}
```

## Deploying

Netlify has made this easy. If you click the deploy button below, it will guide you through the process of deploying it to Netlify and leave you with a copy of the repository in your GitHub account as well.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/hzik/Searchable-text)

## What is Saved?

```json
"indexed_text": {
                    "type": "custom",
                    "name": "Indexed text",
                    "value": "[\"Hi\",\"how\",\"are\",\"you\"]"
                }
```

## Searching by indexed text

You can use `Contains` filter to find the item you need:

`/items?elements.indexed_text[contains]=word`
