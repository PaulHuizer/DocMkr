[Table of contents](toc.md)

<img src="https://github.com/LetsWrappIt/DocMkr/blob/main/images/DocMkr_logo_1280x640.png" width="300" height="150">

DocMkr, short for DocMaker, is an unopinionated, scratch-your-own-itch, yet very powerfull tool, that generates proper PDF documents.

What makes DocMkr so usefull for many:
- It generates beautiful PDF documents
- It supports 'classic' document structures like: Sections, Pages, Headers, Footers, Headings, TableOfContents, Images ... 
- Seperation of styling and content: this allows for sharing and reuse of style templates.
- Support conditional generate process (write 1 tutorial, publish for 10 brands?)
- Support multi file projects. This allows for modular organization of both content and style. This facilitates large document scenarios.
- Very suitable for version control on github for example.


## How does DocMkr work?
The main function of DocMkr is the 'build' process, which takes 2 core files and transforms those into a PDF document.
The first file is a DocMkr Template file, DmTemplate, or dmt.
The second file is a DocMkr Content file, DmContent, or dmc.

DocMkr itself comes in the form of a cli (win/linux/mac). Use your favorite text/html/xml editor (exmample: VsCode) to edit the content and the styling.


## Start tutorial

### Step 1: Get your editor
Pick your favorite text/XML/HTML editor for writing content and styling.

### Step 2: Write a DmContent file
Write a HTML document with some content, this is the DmContent file (dmc).
Example:
```
<html>
<body>
    <section>
        <h1>This is a manual</h1>
        <p>The manual for this device ...</p>
    </section>
</body>
</html>
```
Save as: manual.dmc.html


### Step 3: Write a DmTemplate file
Write a XML document with styling configuration, this is the shortest, and still viable, DmTemplate file (dmt).
```
<docmkr-template>
</docmkr-template>
```
Save as: simple.dmt.xml

### Step 4: Donwload DocMkr cli

You can do that [here](download.md)!


### Step 5: Write a build script

Write a one line script file, to call the cli with proper arguments, something like:

Example:
```
./docmkr.exe build /dmt:simple.dmt.xml /dmc:manual.dmc.html
```

Save as: make-manual.cmd

### Step 6: Build the PDF
Call the build script. It will call DocMkr to build your first PDF document.
From here you can build further and further.



Some links:
- [Get started](getstarted.md)
- [ChangeLog](changelog.md)
