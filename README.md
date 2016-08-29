# theophrastus-stiftung.de

https://jekyllrb.com/ based static generated site

## Quick setup

    gem install jekyll
    bundle install
    bundle exec jekyll serve
    => Now browse to http://localhost:4000

## Edit or Add *.md files

### general Markdown-File Setup

    ---
    layout: page
    title: Pagename
    permalink: /pagename/
    ---

### more navigation hierarchies

#### setup for the 2. hierarchy

    ---
    layout: page
    title: Pagename
    permalink: /parentpagename/pagename/
    subpage: true
    ---

#### setup for the 3. hierarchy

    ---
    layout: page
    title: Pagename
    permalink: /parentparentpagename/parentpagename/pagename/
    subsubpage: true
    ---

### specific content type inclues

#### Links

    {% include link.html link="mailto:info@theophrastus-stiftung.de" linktext="info@theophrastus-stiftung.de" %}

    the file needs to be located in /downloads/
    {% include link.html file="myFile.pdf" linktext="myFile" description="download myFile via click" %}

#### Images

    all images need to be located in /images/
    {% include image.html src="image.jpg" align="left/center/right" width="integer" height="integer" description="some info to this image" breakafter="true" %}

    normal setup:
    {% include image.html src="image.jpg" align="left" width="100" %}

#### Image Folder

    all images within a folder can be outputed via:
    {% image_set images/myFolder %}

### additional content

#### PDFs
all pdfs need to be located in /downloads/:

    ---
    layout: page
    title: Pagename
    permalink: /pagename/
    pdfs:
        - MyDataName.pdf
        - MyDataName2.pdf=I have a caption
    ---

#### Images
all images need to be located in /images/:

    ---
    layout: page
    title: Pagename
    permalink: /pagename/
    images:
        - MyImageName.pdf
        - MyImageName2.pdf=I have a caption
    ---

## Push changes to GitHub

    git add *
    git commit -m "update"
    git push origin master
=> username: theophrastus-stiftung
=> password: XXXXXXXXXXXXXXXXXXXXX