---
toc: true
layout: post
description: A fastpages-powered report.
categories: [markdown]
title: Luma Maincolor Report
---
# Luma Maincolor Report

## Report setup

Report is in the following naming convention:

`YEAR-MONTH-DAY-filename.md`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `filename` is whatever file name you choose, to remind yourself what this post is about. `.md` is the file extension for markdown files.

The first line of the file should start with a single hash character, then a space, then your title. This is how you create a "*level 1 heading*" in markdown. Then you can create level 2, 3, etc headings as you wish but repeating the hash character, such as you see in the line `## File names` above.

## Report Format

We use *italics* for quantitative result.

**bold** is to emphasize the metrics used.

To facilitate copy, will use `code font text`.

Here is [links](https://www.markdownguide.org/cheat-sheet/) format.
 
And here's a footnote [^1] sample, followed by a horizontal rule:

---

## Evaluation Result

We are providing the below metrics:

- False Acceptance Rate **(FAR)**
- False Rejection Rate **(FRR)**

and these are their respective results:

1. *FAR = 0.0*
1. *FRR = 0.476*

## Here is the detailed report:

> This is a quotation

{% include alert.html text="You can include alert boxes" %}

...and...

{% include info.html text="You can include info boxes" %}

## Activation Heatmap

![]({{ site.baseurl }}/images/logo.png "fast.ai's logo")

## Fastai Reference

We download the base model for EfficientNet 

B2 variant:

    # EfficientNet B2
    EfficientNet.from_pretrained('efficientnet-b2')

Python code for training:

```python
learner = Learner(data, model,
                metrics=[accuracy, KappaScore(weights="quadratic")],
                callback_fns=[ShowGraph,
                              partial(SaveModelCallback, monitor='kappa_score', name='best_kappa')]
               )
```


Confusion is generated from below:

```shell
interp.plot_confusion_matrix(figsize=(4,4), dpi=120)
```

Formatting text as YAML:

```yaml
key: value
- another_key: "another value"
```


## Result Table

| FAR | FRR |
| 0.0 | 0.476 |
| 0/100 | 9/2000 |



## Footnotes



[^1]: This is, if any, footnote.

