# ProcessWire ImageExtra

**Designed for use with ProcessWire 3.x**

## About

This module allows you to add additional informations to an image (for example: title, description, link, orientation and any field you may need).

## Usage

For each instance of an image field the field settings will be extended. Navigate to *Admin > Setup > Fields* and edit the desired field. Click on the Input Tab and click on the **"Image Extra Fields ..."** area.
It extends downwards and reveals a form to set up additional custom fields.

The following fields are available by default:

- **description** - image description (core)
- **disable multi language description**
- **caption** - image caption to use for title/alt tag or/and caption, if empty
- **orientation** - image orientation
- **orientation values** - values to use as class names or identifiers for different image orientations
- **link** - image link to internal pages
- **other fields** - here you can add any other field by writing it (separated by comma)

For each of the activated custom fields an own column in the specific table will be created.  
As soon as you added any custom field(s), a table containing all fields appears below.
You can set here a textformatter (e.g. Markdown, Paragraph Stripper, ..) for each field - if you want to. The textformatters have to be installed before.

**Caution:** Just removing a custom field will not erase it, due to data persistence. If you really don't need it anymore you have to delete the column manually.
 
After having added some custom fields to an image field, edit a page which has a template containing this field.
Below each image you get some additional config fields - and for sure it provides multi language support.

## Accessing the values

This is no different than accessing the value of any other field.

```php
$image = $page->image->getRandom();
echo $image->caption;
echo $image->location;
echo $pages->get($image->link)->url;
```
