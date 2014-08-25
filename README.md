# Mezzanine File Collections

Mezzanine File Collection is a simple file container page type for the
Django / Mezzanine CMS.

The Mezzanine's core gallery module only deals with images. I got frustrated
with it, I quickly developed an alternative to handle any filetype.

Most of this app's code is directly inspired from the Mezzanine's core.

## Installation

Installation is quite simple.

    $ pip install mezzanine-file-collections

Add "mezzanine_file_collections" to your list of installed apps. Then migrate
your database. 

Add the desired file types to FILEBROWSER_EXTENSIONS on settings.py. Example:

```
FILEBROWSER_EXTENSIONS = {
    'Folder': [''],
    'Image': ['.jpg','.jpeg','.gif','.png','.tif','.tiff'],
    'Video': ['.mov','.wmv','.mpeg','.mpg','.avi','.rm'],
    'Document': ['.pdf','.doc','.rtf','.txt','.xls','.csv'],
    'Audio': ['.mp3','.mp4','.wav','.aiff','.midi','.m4p', '.ogg'],
    'Code': ['.html','.py','.js','.css']
}
```

That's it.

## Usage

Once installed, just create a new "Media Library" page, and upload your files
the usual way.

The default templates uses Bootstrap's media objects for a basic rendering,
but it's very easy to overwrite it. Just look into the template.
