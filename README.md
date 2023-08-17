# README

<!-- badges: start -->

<!-- badges: end -->

There are many options for formatting exported Qualtrics data. The two examples show here demonstrate importing labeled data verses importing CSV or Excel data formats. There are pros and cons to each approach. The data in this repository is randomly generated test data.

Labeled data are imported in the `labeled_data.qmd` code notebook.

CSV data are imported in the `csv_data.qmd` code notebook.

### Shortcut

The coding technique for importing labeld data uses the haven package

```         
my_df  <- read_sav("data/my_file.sav")

# convert labeled data to factors in R
my_df |> 
  mutate(across(is.labelled, ~ as_factor(.x), .names = "{.col}_label"))
```

### Example

![Qualtrics Labeled data: imported via haven.](output/viz_as_imported_labeled_data.svg)
