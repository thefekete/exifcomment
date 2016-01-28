# exifcomment

Edits EXIF comment tag in jpegs. Uses yad for gui, exiftool to edit tags and convert (imagemagic) for image resizing. Opens a window with yad. Click OK to save comment to image, click cancel to skip editing an image & press escape or close window to quit editing altogether.

## Usage
```sh
    exifcomment $0) [options] image [image2 ...]
```

## Options
```
-s, --skip          skip pictures that already have the comment flag
-b, --backup        save a backup of image suffixed with '_original'
-c, --ctag tag      write comments to tag other than '$ctag'
-h, --help          print this message and exit
```

## Examples
Edit comment on `mydog.jpg`:
```sh
exifcomment mydog.jpg
```

Edit comment on `mydog.jpg`, but keep a backup (`mydog.jpg_original`):
```sh
exifcomment --backup mydog.jpg
```

Edit comments on all jpegs in `company_picnic/`:
```sh
exifcomment company_picnic/*.jpg
```

Edit comments on jpegs in `family_reunion/` that don't have one yet:
```sh
exifcomment --skip company_picnic/*.jpg
```
