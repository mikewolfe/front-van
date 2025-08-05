# Frontiers in Vancouver-Style Quarto Template

## Creating a New Article

To create a new article using this format:

```bash
quarto use template mikewolfe/front-van
```

This will create a new directory with an example document that uses this format.

## Using with an Existing Document

To add this format to an existing document:

```bash
quarto add mikewolfe/front-van
```

Then, add the format to your document options:

```yaml
format:
  front-van-pdf: default
```    

## Options

The default setting for class options follows the `frontiers.tex` file that
comes from the journal, that is:

```yaml
classoption: utf8
```

The `Frontiers-Vancouver.cls` appears to support support several other options
including `draft`, `final`, `a4paper` etc. but they have not been tested so 
use at your own risk.

In order for the author affiliations to be properly formatted, each affiliation
must use a number `1`, `2`, etc. as the id field.

The corresponding authors is set with
```yaml
attributes:
  corresponding: true
```
However, multiple corresponding authors is not currently supported for the pdf
format.

This template supports `pdf`, `word`, and `html` output. Both `pdf` and `word`
are based on the files from the journal. The `html` output is a quarto default
output but with the Vancouver citation style.

The word output does not format the authors properly and must be edited by hand
after generating.

## Example

Here is the source code for a minimal sample document: [template.qmd](template.qmd).

Which renders to this:
<!-- pdftools::pdf_convert('template.pdf',pages = 1) -->
![[template.qmd](template.qmd)](template_1.png)

## License
This modifies the Frontiers in Template LaTeX and Word templates, available at
<https://www.frontiersin.org/guidelines/author-guidelines#writing-and-formatting>.

This template was created following the excellent guide by Christopher Kenny:

T. Kenny, Christopher. 2023. “Creating Quarto Journal Article Templates.” July 1, 2023. 
https://christopherkenny/posts/2023-07-01-creating-quarto-journal-articles.