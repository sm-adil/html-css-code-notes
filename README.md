# rit-hassan-code-notes

Here we have all the code notes we"ll be using during camp

## HTML (Hypertext Markup Language)

- `!DOCTYPE html` Tells browser that the document beibg used is written in html5 syntax

- `<html lang="en">` Defines the begining and end of the html webpage. `lang` attribute defines the document language

    ```
    <html>
        ...
    </html>
    ```

- `<head>` Initial content to be executed when page is loaded. We defines loading of external resources (css, js, icon etc) and static markup.

    ```
    <head>
        ...
    </head>
    ```
    - `<meta>` Provides meta data of the webpage (description, character set etc)

        ```
        <meta name="description" content="Some description"/>
        ```
    - `<title>` Defines the title of the webpage

        ```
        <title>I am a title</title>
        ```
    - `<link>` Used to import external resources (css, fonts) into webpage

        ```
        <link rel="stylesheet" href="file.css">
        ```

- `<body>` Defines the document"s body, contains all the content of page (text, images, links etc)

    ```
    <body>
        ...
    </body>
    ```
    - `<div>` Defines the part of the webpage, mostly used to break the html elements into parts

        ```
        <div>
            ...
        </div>
        ```
    - `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>` Heading tags, each tag has different font-size & font-weight

        ```
        <h1>Heading h1</h1>

        <h2>Heading h2</h2>

        <h3>Heading h3</h3>

        <h4>Heading h4</h4>

        <h5>Heading h5</h5>

        <h6>Heading h6</h6>
        ```
    - `<p>` Defines the paragraph of text/numbers/characters

        ```
        <p>Paragraph</p>
        ```
    - `<a>` Anchor tag, used to add hyper links to webpage
    
        ```
        <a href="https://new-link.com">Link</a>
        ```
    - `<img>` Display images onto webpage

        ```
        <img src="file.jpg" alt="alternative name">
        ```
    -  `<form>` Used in data interaction. Users can add or upload text/email/number/password/file

        ```
        <form>
            ...
        </form>
        ```
        - `<input>` Takes in text/files from the user & can be used to store these data elsewhere

            ```
            <input type="text" placeholder="Text placeholder" value="Some value" />

            <input type="email" placeholder="Email placeholder" value="Some value" />

            <input type="password" placeholder="Password placeholder" />

            <input type="checkbox" value="Checkbox value" />

            <input type="radio" placeholder="Radio value" />

            <input type="file" />
            ```
    - `<button>` Provides a button in order to interact with webpage

        ```
        <button>I am a button</button>
        ```
    - `<script>` Will add JavaScript into the html webpage

        ```
        <script>
            ...
        </script>

        or

        <script src="file.js">
        ```

## CSS (Cascading Stylesherts)

- Adding `css` to `html`

    - `Inline`: Within the html elements

        ```
        <h1 style="color: red">
        ```
    - `Internal`: Using `<style>` tag

        ```
        <style>
            h1 {
                color: red;
            }
        </style>
        ```
    - `External`: Use`<link>` tag to import css file into html

        ```
        <link rel="stylesheet" href="file.css">
        ```

- `Selectors`: These are the attributes which will be targeted to add styling properties

    - `class`

        ```
        .class-name {
            ...
        }
        ```
    - `id`

        ```
        #id-name {
            ...
        }
        ```
    - `element` (h1, img, body etc)

        ```
        h1 {
            ...
        }
        ```
- `Colors`

    - `color`
        ```
        h1 {
            color: pink;
        }
        ```
    - `background-color`

        ```
        div {
            backfround-color: yellow;
        }
        ```

- `Text`

    - `font-size`: Customize size of the fonts of the webpage

        ```
        h2 {
            font-size: 16px;
        }
        ```
    - `font-weight`: Customize weight of the fonts

        ```
        h2 {
            font-weight: 700;
        }
        ```

- `Box Model`: CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content

    - `content`: HTML markup (text, image, div's etc)

        ```
        <div>
            ...
        </div>
        ```
    - `padding`: Space around the content

        ```
        div {
            padding-top: 20px;
            padding-bottom: 20px;
            padding-left: 20px;
            padding-right: 20px;
        }

        or

        div {
            padding: 20px;
        }
        ```
    - `border`: Goes around the padding and content

        ```
        div {
            border-width: 2px;
            border-style: solid;
            border-color: red;
        }

        or

        div {
            border: 2px solid red;
        }
        ```
    - `margin`: Creates space around content, outside of any defined borders

        ```
        div {
            margin-top: 20px;
            margin-bottom: 20px;
            margin-left: 20px;
            margin-right: 20px;
        }

        or

        div {
            margin: 20px;
        }
        ```

- `box-shadow`: Adds one or more shadows to an element. Uses horizontal-offset, vertical-offset, bur-ratio, spread-radius & color

    ```
    div {
        box-shadow: 3px 3px 5px 6px #ccc;
    }
    ```

- `Pseudo class`: Additional classes which can be targeted with normal html attribures

    ```
    div:hover {
        background-color: pink;
    }
    a:active {
        color: red;
    }
    ```

- `Media Queries`: Include a block of CSS properties only if a certain condition is true

    ```
    @media screen (max-width: 700px) {
        div {
            ...
        }
    }

    @media screen (max-height: 500px) {
        div {
            ...
        }
    }
    ```

- `CSS Grid System`: Allows us to quickly create flexible, two dimensional layouts

    ```
    div {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        justify-content: center;
        align-content: centr;
    }

    // Responsive grid
    div {
        display: grid;
        grid-gap: 20px;
        grid-template-columns: repeat(auto-fit, minmax(175px, 1fr));
        justify-content: center;
        align-content: centr;
    }
    ```