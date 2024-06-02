# Posit::Conf2024 Template for Quarto

In order to make sure the background pictures work in Connect, feel free to use
this code to create the manifest file. It will contain the needed references 
to the pictures.

```r
app_files <- fs::dir_ls()
app_files <- app_files[!grepl("qmd", app_files)]
app_files <- app_files[!grepl("rsconnect", app_files)]
rsconnect::writeManifest(
  appPrimaryDoc = "positconf2024-template.html",
  appFiles = app_files
)
```