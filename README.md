CONTENTS OF THIS FILE
---------------------

 * summary
 * requirements
 * installation
 * configuration
 * usage
 * FAQ
 
SUMMARY
-------

Islandora Featured Collection

The Islandora Featured Collection module adds a "Featured Objects" collection to
an Islandora repository, and adds a Featured Objects block to the block list
using the Views module. This block is able to point to the Featured Objects
collection and load objects from it, with thumbnails and descriptions.

REQUIREMENTS
------------

Views 3.0
Islandora 7.x with the following modules installed:
 * Islandora Collection Solution Pack
 * Islandora Solr Search
 * Islandora Solr Views

INSTALLATION
------------

Ensure that all prerequisite modules are installed, then install the Islandora
Featured Collection module.

CONFIGURATION
-------------

In a typical installation of Islandora, the Featured Objects block should be
configured and ready to go. However, it may not be compatible out-of-the-box
with certain Solr configuration schema.

If you find the Featured Objects block isn't working, you can check the settings
for it at your site's admin/structure/views/view/featured_collection_blocks/edit
page. Here, you may have to redirect two fields to properly fit your schema:

 * Islandora Solr: mods_abstract_ms needs to point to the object MODS form's Description/Abstract field.
 * Islandora Solr: RELS_EXT_isMemberOfCollection_uri_mt needs to point to the object RELS-EXT's isMemberOfCollection field.

USAGE
-----

To add an object to the Featured Objects block, simply share it with the
Featured Objects collection. It will automatically be added to the block.

FAQ
---

Q. If I uninstall the Islandora Featured Collection module, will the Featured
Objects collection be removed?

A. No, the Featured Objects collection is left untouched to prevent object loss.
The collection must be manually removed.