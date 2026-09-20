# FAVF LaTeX package

This is a LaTeX package that contains standard LaTeX definitions to be used at the FAVF lab.
The package's file name is **favf_definitions.tex**.

# FAVF Wiki

Please find more information on the FAVF Wiki page https://www2.tu-ilmenau.de/favfwiki/wiki/index.php?title=FAVF_Latex_Package .


# Usage

There are two ways of using this LaTeX package depending on the type of document that you are writing.

If you are writing a document that should be maintained over a longer time frame (e.g., years), you should import it from this Git repository via Git submodules. 
In this case, **favf_definitions.tex** is put into a subdirectory (the submodule's subdirectory in your LaTeX project).
This way should be used for thesis templates, style guides and similar documents.

If you are writing a document that should only be compilable during a shorter amount of time (e.g. months),
you should put **favf_definitions.tex** directly into your LaTeX project's root directory. 
This way should be used for papers, project proposals and similar documents.

## Package in subdirectoy (e.g. with Git submodules)

Suppose the file **favf_definitions.tex** is in a subdirectory **favf_latex_package** (just an example).
Then, insert the following line into your main .tex file.

```tex
\input{favf_latex_package/favf_definitions}
```

## Package in LaTeX project's root directory

Insert the following line in the header of your main .tex file:

```tex
\input{favf_definitions}
```


# Why not a .sty file?

Unfortunately, there are problems when using .sty files from subdirectories (e.g., with Git submodules).
Hence, it was decided to provide this LaTeX package not as a .sty file but as a .tex file whose content should be included via **\input{...}**.
