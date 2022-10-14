Webform Share
========
Webform Share enables you to export the configuration for an existing webform
and either import into another webform or use it to create default webform
components for a webform-enabled content type.

There are three main use cases for this module:

1. To build a webform on a development site and import it into production.
2. To use a set of components from a form in other forms on your site.
3. To define and apply a default set of webform components and settings for each
content-type.

### Differences from Drupal 7
- Exports as JSON array rather than PHP array definiton so no need to use the
`eval()` function; because of this, there is no upgrade path.
- Content type defaults moved from publishing options to Webform tab.
- Configuration moved to Configuration Management.
- Some re-wording to improve clarity.

Requirements
------------
This module requires that the following modules are also enabled:

- [Webform](https://github.com/backdrop-contrib/webform)

Installation
------------
- Install this module using the official Backdrop CMS instructions at
  https://docs.backdropcms.org/documentation/extend-with-modules.
- Ensure the permission "Configure Webform Share" is granted to relevant users.

Usage
-----
### Export
1. Navigate to the node and click the "Webform" tab
2. Click the "Export" button

The webform configuration will download in a .json file

### Import
1. Navigate to an existing or new node of a content type where webforms are
enabled and click the "Webform" tab
2. Click the "Import" button
3. Paste the contents of the .json file you downloaded into the "Import code"
text area.
4. If you want to keep any existing components in your webform then check the
"Keep existing components that are not includeded in the import" option.
5. If you want to keep the email and form settings and just override the
components and conditionals check the "Update components and conditionals only"
option.

### Setting default webform components for content type
1. Export the webform configuration that you want to use as the default
2. Navigate to the Configure tab for the content-type you wish to set webform
defaults for.
for. (i.e. `admin/structure/types/manage/[content_type]/configure`)
3. Click on the "Webform" sub-tab.
4. Note that if you haven't previously enabled Webforms for this content-type
then you will need to enable, "Save Content Type" and return to the "Webform"
sub-tab.
5. Paste the contents of the .json file you downloaded into the "Webform
default components" text area and save the content-type.
6. Create a new node of that content type and the webform will be automatically added.

Issues
------
Bugs and Feature Requests should be reported in the Issue Queue:
https://github.com/backdrop-contrib/webform_share/issues.

Current Maintainers
-------------------
- [Martin Price](https://github.com/yorkshire-pudding) - [System Horizons](https://www.systemhorizons.co.uk)
- Collaboration and co-maintainers welcome!

Credits
-------
- Ported to Backdrop CMS by - [Martin Price](https://github.com/yorkshire-pudding) - [System Horizons](https://www.systemhorizons.co.uk).
- Port sponsored by [System Horizons](https://www.systemhorizons.co.uk).
- Originally written for Drupal by [Alan D.](https://www.drupal.org/u/alan-d).

License
-------
This project is GPL v2 software.
See the LICENSE.txt file in this directory for complete text.