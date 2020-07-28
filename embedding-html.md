# Embedding HTML

## HTML Basics

Although Markdown may be very easy to use, it is somewhat limited in what it can do. Luckily, it is very easy to include HTML in your Markdown files, which opens up many more options for customization of your website.

HTML is made up of elements and tags. An **element** is a piece of the website's content and either constitutes text enclosed by two tags or is a tag itself (this is called an empty element because it contains no text, just a tag). A **tag** instructs the browser how to display elements and is enclosed in angle brackets like this: `<tag>`. Except for standalone tags, all tags need a matching end tag in order to define where the element ends. An end tag looks like this: `</tag>`.

- Example element: `<p>text</p>`
- Example empty element: `<br>`

Some HTML elements contain **attributes**. Attributes contain additional information about an element and go in a start tag like this: `<tag attribute=___>`

- Example start tag with an attribute: `<a href="index.md">`

## Embedding HTML in Markdown

Because Markdown is translated into HTML before being displayed, HTML elements can be very easily integrated into Markdown files. All you need to do is start typing in HTML. Here are some examples of what you can do with HTML that you can't with Markdown.

### Underlined Text

First of all, while Markdown does not support <ins>underlined text</ins>, HTML does.

**HTML:** `<ins>Underlined text</ins>`<br>**Browswer:** <ins>Underlined text</ins>

### Line Breaks

You can also make single-spaced line breaks in HTML. Normally, Markdown only supports double-spaced line breaks, so this is useful for keeping lines close together.

**HTML:** `Line 1<br>Line 2`<br>**Browser:**<br>Line 1<br>Line 2

### Colors

You can color text or give text colorful backgrounds or borders using HTML. This can be done using the `<span>` tag, as well as the attribute `style=`.

<ins>**Text Color:**</ins>

**HTML:** `<span style="color:red;">Red Text</span>`<br>**Browser:** <span style="color:red;">Red Text</span>

<ins>**Background Color:**</ins>

**HTML:** `<span style="background-color:yellow;">Red Text</span>`<br>**Browser:** <span style="background-color:yellow;">Red Text</span>

<ins>**Border Color:**</ins>

**HTML:** `<span style="border:2px solid red;">Red Text</span>`<br>**Browser:** <span style="border:2px solid red;">Red Text</span>

### Buttons

Buttons are always fun to add to websites. You can do this with the `<button>` tag. This one looks a little more complicated (it actually uses a little JavaScript), but it works perfectly fine in any Markdown or HTML file.

**HTML:** `<button onclick="window.location.href='index.md'">Home</button>`<br>**Browswer:** <button onclick="window.location.href='index.md'">Home</button>

### Clickable Images

To make clickable images, you must embed one element inside another. This can be done in the following format:

```
<tag1>
  <tag2>
</tag1>
```

In this case, `<tag2>` is an empty element contained in the element defined by `<tag1>`.

To make our clickable image, we will start with the `<a>` tag on the outside, which creates a hyperlink. The start tag will also include the `href=` attribute, which makes the element into a link. You can replace `index.md` with any other link or relative link (remember, a relative link goes to another page in the same repo).

```
<a href=index.md>
</a>
```

*Remember to include a space in* `<a href=>`

Now, on the inside, we can put the `<img>` tag, which works similarly to the image function of Markdown. After `<img>`, you must include the image source, and may include alternative text and/or specify the image size:

- **The image source:** This is the file name of the image: `src="image.png"`<br>
- *The alternative text:* This is what users will see if the image doesn't load: `alt="Datacts Logo"`<br>
- *Image size:* This adjusts the size of the image: `style="width:100px;height:100px;"`

**The `<img>` tag put together:** `<img src="image.png" alt="Datacts Logo" style="width:100px;height:100px;">`

*Remember to include quotation marks and to use two semicolons in* `"width:100px;height:100px;"`

It's usually recommended to upload images directly into your repo so you can easily reference them. Click **HERE** (USE LINK WITH # TO FIND SPECIFIC PART) to learn how to add images to your repo.

---

The final result:

**HTML:**

```
<a href="index.md">
  <img src="image.png" alt="Datacts Logo" style="width:100px;height:100px;">
</a>
```

**Browswer:**

<a href="index.md">
  <img src="image.png" alt="Datacts Logo" style="width:100px;height:100px;">
</a>
