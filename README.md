# 40kbible
## By Shoshana & co.

## Synopsis
In their senior year of high school, most students are trying to determine career paths. Unfortunately, to even understand the key problems in a field substantial knowledge is usually required, knowledge that students often do not acquire until completing an undergraduate program.

The solution is a career bible curated by the Atlas fellows. Many have expressed interest in aiding secondary school education, and most fellows have specialized knowledge in at least one field, such as philosophy, economics, policy, chemistry, or subfields of mathematics and computer science. In the past this has made collaboration between two or three fellows pretty cool. The aim of this project is a collaboration between two or three dozen fellows, making something *really* cool.

## Setup
We are writing the book in Markdown and using [panoc](https://pandoc.org/installing.html) to convert it to a pdf through `pdfLaTeX` (TeX Live). I recommend the [Obsidian](https://help.obsidian.md/Getting+started/Download+and+install+Obsidian) editor.

## Structure
```shell
40kbible/
├── 40kBible.pdf
├── bible
│   ├── applied_mathematics
│   │   ├── numerical_methods.md
│   │   └── quantitative_trading.md
│   └── index.md
├── defaults.yaml
└── README.md
```
## Contributing
To add a new field, go to `bible/index.md` and insert a new subtitle. Make a directory with the `camel_case` name of the field. To add a career insert a bullet point under its field in `bible/index.md` with a `[hashtag](#link)` to the corresponding file, and include it in the `input-files` in `defaults.yaml`. Make sure your file ends in a new line.

Keep fields and careers in lexicographic order.

## Building
Run `pandoc --defaults defaults.yaml`.