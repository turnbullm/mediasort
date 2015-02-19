Mediasort
=========

Manage filenames and metadata of your media files

Go easy
-------

I'm an absolute beginner at writing bash scripts. Please let me know of any improvements. Cheers!

Dependencies
------------

### exiv2

Command line utility to manage image metadata

http://www.exiv2.org/

```
brew install exiv2
```

Installation
============

```
cd ~/bin/
wget github.com/mediasort-update-filename.sh
wget github.com/mediasort-update-metadata.sh
chmod +x mediasort-update-filename.sh
chmod +x mediasort-update-metadata.sh
```

Usage
=====

Update filename
---------------

```
cd /path/to/media/
mediasort-update-metadata
```

Rename files to: `{{date}} {{name}}.{{ext}}`

{{date}} is in the format: `YYYYMMDD_HHMMSS`

*.jpg files;*

- {{date}} = 'date taken' exif metadata if available, fallback to 'date file created'
- {{name}} = from 'keywords' exif metadata

*other files;*

- {{date}} = date file created
- {{name}} = original filename

Update metadata
---------------

```
cd /path/to/media/
mediasort-update-filename
```

Set date file created, exif date taken and keywords

Files must be in the format: `YYYYMMDD_HHMMSS keyword 1, keyword 2.jpg`