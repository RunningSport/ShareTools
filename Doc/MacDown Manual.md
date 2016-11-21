# Markdown
* 使用 **Markdown** 写文档，效率更高，作者只需要关注文本内容，外在表现由浏览器去渲染，这样忽略掉格式，只关注内容的方式，可以大大提高写作的效率。

* **Markdown** 的规则很简单，花几分钟时间就可以上手了，后文有详细的介绍。

* 苹果机上写**Markdown**文档，首推开源免费的 **MacDown**，时时展现，很方便，很好用。详细介绍见下文。

# MacDown

![MacDown logo](http://macdown.uranusjr.com/static/base/img/logo-160.png)

Hello there! I'm [**MacDown**][arbitrary_id], the open source Markdown editor for OS X.

Let me introduce myself.

## 1. Markdown and I

**Markdown** is a plain text formatting syntax created by John Gruber,aiming to provide a easy-to-read and feasible markup. The original Markdown syntax specification can be find [here](http://daringfireball.net/projects/markdown/syntax).

**Macdown** is created as a simple-to-use editor for Markdown documents. I render your Markdown contents real-time into HTML,and display them in a preview panel.

![MacDown Screenshot](http://d.pr/i/10UGP+)

I support all the original Markdown syntaxes. But I can do so much more! Various popular but non-standard syntaxes can be turned on/off from the [**Markdown** preference pane](#markdown-pane)

You can specify extra HTML rendering options through the [**Rendering** preference pane](#rendering-pane)

You can customize the editor window to you liking in the [**Editor** preferences pane](#editor-pane)

You can configure various application (that's me!) behavious in the [**General** preference pane](#general-pane).

## 2. The Basics
Before I tell you about all the eatra syntaxes and capabilities I have, I'll introduce you to the basics of standard markdown. If you already know markdown, and want to jump straight to learning about the fancier things I can do. I suggest you skip to the [**Markdown** preference pane](#markdown-pane). Let's jump right in.

### Line Breaks
To force a line break, put two spaces and a newline (return) at the end of the line.

	These lines  
	won't break
	
	These lines
	will break

### Strong and Emphasize

**Strong**: `**Strong**` or `__Strong__` (Command-B)  
*Emphasize*: `*Emphasize*` or `_Emphasize_` [^emphasize] (Command-I)

### Headers (like this one!)

	Header 1
	========
	
	Header 2
	--------
	
or 

	# Header 1
	## Header 2
	### Header 3
	#### Header 4
	##### Header 5
	###### Header 6
	
### Links and Email

#### Inline
Just put angle brackets around an email and it becomes clickable: <aaazhibei@gmail.com>  
`<aaazhibei@gmail.com>`

Same thing with urls: <https://www.github.com>  
` <http://www.github.com>`

Perhaps you want to some link text like this: [GitHub Website](https://www.github.com "Title")  
`[GitHub Website](http://www.github.com "Title")` (The "Title" is optional)

#### Reference style
Sometimes it looks too messy to include big long urls inline, or you want to keep all your urls together.

Make [a link][arbitrary_id] `[a link][arbitrary_id]` then on it's own line anywhere else in the file: `[arbitrary_id]: http://www.github.com "Title"`

If the link text itselft would make a good id, you can link [like this][] `[like this][]`, then on it's own line anywhere else in the file:
`[like this]: https://www.github.com`

[arbitrary_id]: http://macdown.uranusjr.com/
[like this]: http://macdown.uranusjr.com/ 

### Images

#### Inline
`![Alt Image Text](path/or/url/to.jpg "Optional Title"`

#### Reference Style
`![Alt Image Text][image-id]`  
on it's own line eleswhere:  
`[image-id]: path/or/url/to.png "Optional Title"`

### Lists

* Lists must be preceded by a blank line (or block element)
* Unordered lists start each item with a `*`
- `-` works too
	* Indent a level to make a nested list
		1. Ordered lists are supported.
		2. Start each item (number-period-space) like `1. `
		32. It doesn't matter what number you use, I will render them sequentially
		33. So you might want to start each line with `1. ` and let me sort it out

Here is the code:

```
* Lists must be preceded by a blank line (or block element)
* Unordered lists start each item with a `*`
- `-` works too
	* Indent a level to make a nested list
		1. Ordered lists are supported.
		2. Start each item (number-period-space) like `1. `
		32. It doesn't matter what number you use, I will render them sequentially
		33. So you might want to start each line with `1. ` and let me sort it out
```

### Block Quete

> Angle brackets `>` are used for block quotes.  
Technically not every line needs to start with a `>` as long as 
there are no empty lines between paragraphs.  
> Looks kinda ugly though.

> > Block quetes can be nested.
> > > Multiple Levels
> 
> Most markdown syntaxes work inside block quetes.
> 
> * Lists
> * [Links][arbitrary_id]
> * Etc.

Here is the code:

```
> Angle brackets `>` are used for block quotes.  
Technically not every line needs to start with a `>` as long as 
there are no empty lines between paragraphs.  
> Looks kinda ugly though.

> > Block quetes can be nested.
> > > Multiple Levels
> 
> Most markdown syntaxes work inside block quetes.
> 
> * Lists
> * [Links][arbitrary_id]
> * Etc.

```

### Inline code
`Inline code` is indicated by surrounding it with backticks:  
`` `Inline code` ``

If your ``code has `backticks` `` that need to be displayed, you can use double backticks:  
```` ``Code whith `backticks` `` ```` (mind the spaces preceding the final set of backticks)

### Block Code
If you indent at  least four spaces or one tab, I'll display a code block.

	print('This is a code block')
	print('The block must be preceded by a blank line')
	print('Then indent at least 4 spaces or 1 tab')
		print('Nesting does nothing. Your code is dispalyed Literally')
		
I also know to do something called [Fenced Code Blocks](#fenced-code-block) which I will tell you about later.

### Horizontal Rules
If you type three asterisks `***` or three dashes `---` on a line, I'll display a horizontal rule:  

***  

---  

--------

## <a name="markdown-pane"></a>3. The Markdown Preference Pane
This is where I keep all preferences related to how I parse markdown into html.
![Markdown preferences pane](http://d.pr/i/RQEi+)

### Document Formattong
The ***Smartypants*** extension antomatically transforms straight quetes (`"` and `'`) in your text into typographer's quotes (`“`,`”`,`‘`,and `’`) according to the context. very useful if you are a typography freak like I am. Quqte and Smartypants are syntactically incompatible. If both are enabled, Quote takes precedence.

### Block Formatting

#### Table
This is a talbe:

First header | Second header
------------ | ------------
Content Cell | Content Cell
Content Cell | Content Cell

You can align cell contents with syntax like this:

| Left Aligned | Center Aligned | Right Aligned |
|:------------ |:--------------:| -------------:|
| col 3 is     | some wordy text| $1600         |
| col 2 is     | centered       | $12           |
| zebra strips | are neat       | $1            |

The left- and right-most pipes (`|`) are only aesthetic, and can be omitted. The spaces don't matter,either. Alignment depends solely on `:` marks.

#### <a name="fenced-code-block"> Fenced Code Block</a>
  
This is fenced code block:

```
print('Hello world!')
```

You can also use waves (`~`) instead of backticks (`` ` ``):

~~~
print('Hello world!')
~~~

You can add an optional language ID at the end of the first line. The language ID will only be used to highlight the code inside if you tick the ***Enable highlighting in code blocks*** option. This is what happens if you enable it:

![Syntax highlighting example](http://d.pr/i/9HM6+)

I support many popular languages as well as some generic syntax descriptions that can be used if your language of choice is not supported. See [relevant sections on the official site](http://macdown.uranusjr.com/features/) for a full list of supported syntaxes.

### Inline Formatting
The following is a list of optional inline markups supported:

Option name         | Markup           | Result if enable       |
--------------------|------------------|------------------------|
Intra-word emphasis | So A\*maz\*ing   | So A<em>maz</em>ing    |
Strikethrough       | \~~Much wow\~~   | <del>Much wow</del>    |
Underline [^under]	| \_So doge\_      | <u>So doge</u>         |
Quote [^quote]      | \"Such editor\"  | <q>Such editor</q>     |
Highlight           | \==So good\==    | <mark>So good</mark>   |
Superscript         | hoge\^(fuga)     | hoge<sup>fuga</sup>    |
Autolink            | http://t.co      | <http://t.co>          |
Footnotes           | [\^4] and [\^4]: | [^4] and footnote 4    |

[^4]: You don't have to use a number. Arbitrary things like `[^footy note4]` and `[^footy note4]:` will also work. But they will *render* as numbered footnotes. Also, no need keep your footnotes in order, I will sort out the order for you so they appear in the same order they were referenced in the text body. You can even keep some footnotes near where you referenced them, and collect others at the bottom of the file in the traditional place for footnotes.

## <a name="rendering-pane"></a>4. The Rendering perference Pane
This is where I keep preferences relating to how I render and style the parsed markdown in the preview window.
![Rendering preferences pane](http://d.pr/i/rT4d+)

### CSS
You can choose different css files for me to use to render your html. You can even customize or add your own custom css files.

### Syntax Highlighting
You have already seen how I can syntax highlight your fenced code blocks. See the [Fenced Code Block](#fenced-code-block) section if you haven't! You can alse choose different themes for syntax highlighting.

### TeX-like Math Syntax
I can also render TeX-like math snytaxes, if you allow me to.[^math] I can do inline math like this: \\( 1 + 1 \\) or this (in MathML):<math><mn>1</mn><mo>+</mo><mn>1</mn></math>, and block math:

\\[
	A^T_S = B
\\]

or (in MathML)

<math display="block">
	<msubsup><mi>A</mi> <mi>S</mi> <mi>T</mi></msubsup>
	<mo>=</mo>
	<mi>B</mi>
</math>

### Tast List Syntax
1. [x] I can render checkbox list syntax
	* [x] I support nesting
	* [x] I support ordered *and* unordered lists
2. [ ] I don't support clicking checkboxes directly in the html window

### Jekyll front-matter
If you like, I can display Jekyll front-matter in a nice table. Just make sure you put the front-matter at the very beginning of the file, and fence it with `---`. For example:

```
---
title: "Macdown is my friend"
date: 2016-11-04 15:51:00
---
```

## <a name="general-pane"></a>5. The General Preferences Pane
This is where I keep preferences ralated to application behavior.
![General preferences pane](http://d.pr/i/rvwu+)

The General Preferences Pane allows you to tell me how you want me to behave. For example, do you want me to take sure there is a document open when I launch? You can also tell me if I should constantly update the preview window as you type, or wait for you to hit `Commond-R` instead. Maybe you prefer your editor window on the right? Or to see the word-count as you type. This is also the place to tell me if you are interested in pre-releases of me, or just want to stick to better-tested official releases.

## <a name="editor-pane"></a>6. The Editor Preference Pane
This is where I keep preferences related to the behavior and styling of the editing window.
![Editor preferences pane](http://d.pr/i/6OL5+)

### Styling
My editor provides syntax highlighting. You can edit the base font and the coloring/sizing theme. I provided some default themes (courtesy of [Mou](http://25.io/mou/)'s creator, Chen Luo) if you don't know where to start.

You can also edit, or even add new themes if you want to! Just click the ***Reveal*** button, and start moving things around. Remember to use the correct file extension (`.styles`), though. I'm picky about that.

I offer auto-completion and other functions to ease your editing experience. If you don't like it, however, you can turn them off.

## 7. Hack On
That's about it. Thanks for listening. I'll be quiet from now on (unless there's an update about the app- I'll remind you for that!).

Happy writing!

[^emphasize]: If  **Underlines** is turned on, `_this notation_` will render as underlined instead of emphasized

[^under]: If **Underline** is disabled `_this_` will be rendered as *emphasized* instead of being underlined.

[^quote]: **Quote** replaces literal `"` characters with html `<q>` tags. **Quote** and **Smartypants** are syntactically incompatible. If both are enabled, **Quote** takes precedence. Note that **Quote** is different from *blockquote*, which is part of standard Markdown.

[^math]: Internet connection required.