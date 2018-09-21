# MarkdownX
MarkdownX is a project to make Markdown have even better features. A `.mdx` file is a `.zip` file renamed with the following files:

```
- manifest.json (REQUIRED)
- index.md (at least one md or mdj* file must be present, can be in subfolders)
- styles.css or theme.json (one is required, but cannot have both)
- image.png (any image assets needed for the md or mdj files, can be in subfolders)
- images [
      - image2.jpg (this image is in a subfolder, not required)
   ]
- pages [
      - text.md (this md file is in a subfolder, not required, images and links are relative to the folder)
   ]
* An mdj file is a JSON file that contains machine-readable formatting for Markdown. Easy to generate, but hard for humans to read.
```

## Extra Markdown Features
MDX also has a few more features to be more compatible with popular text editors.

### Underline, strike and super/subscript

Underlined text is wrapped by double underscores:

```
Underlined __text is wrapped__ by double underscores.
```
Striked text is wrapped by double hyphens:

```
Striked --text is wrapped-- by double hyphens.
```
Superscript is wrapped by `^` characters. Subscript is wrapped by `^^` strings.

```

This text is ^superscript!^ This text is ^^subscript!^^
```

### Color, font and font size
Colored text is wrapped with `{#EE8800}` and `{#}`

```
This text is {#FF0000}red!{#} This text is {#EE8800}orange!{#}
```
Highlighted text is wrapped with `{hEE8800}` and `{h}`

```
This text is highlighted {hFF0000}red!{h} This text is highlighted {hEE8800}orange!{h}
```

Text with a different font is wrapped with `{)Times New Roman}` and `{)}`

```
This text is {)Arial}sans-serif{)} This text is {)monospace}monospace!{)}
```

Text with a different font size is wrapped with `{(12}` and `{(}`

```
This text is {(50}HUGE{(} This text is {(5}tiny{(}
```

### Image Formatting

Images with a different size should have the new width (in pixels, in curly brackets) after the URL

```
![image](https://path.to/image.png{150})
```

Images with a filter should have the filter (in CSS `filter` form) before the image in curly brackes with a `~` character.

```
!{~saturate(20) sepia(0.2)}[image](https://path.to/image.png)
```

### Paragraph Styling

Paragraphs can have indents in front of them in curly brackets with a `>` character:

```
{>2} This paragraph has two indents!
{>4} This one has four!
```

Paragraphs can have alignment info in front of them in curly brackets with a `<` character. Supported values are l(eft), r(ight), c(enter), j(ustify). You can use either the first letter or the full word.

```
{<c} This paragraph is centered!
{<right} This paragraph is right-aligned!
```

Paragraphs can be positioned and sized with square brackets with a `%` sign at the beginning. The measurements are precents of the viewport. Up to four numbers, seperated by commas, in order are top position, left position, width, height.

```
%[10,10,80,80] This paragraph has a 10% margin on all sides.
```

## What can I use to view, create and edit MDX files?

Currently, nothing, but we plan to change this in the near future.
