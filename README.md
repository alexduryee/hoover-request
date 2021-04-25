# hoover-request

Created by @alexduryee for Hoover Institution.
Compatible with ArchivesSpace 2.8.1.

## New Features

- Replaces the default behavior of the PUI Request button with a link to the collection's Aeon page.
- If no Aeon page is present, link to Stanford's help page instead.

## Using the Plugin

Add `"hoover-request"` to the array in `AppConfig[:plugins]` in your `config/config.rb`

## Customizing the Plugin

The Aeon URL can be modified by editing the `request_url` in `_request_page_action.html.erb`, and the parameters in the same file.

Note that, by design, the Aeon link will only work for Resources with an EAD ID.  Non-Resource pages will have their Requests sent to the help page.  These Request buttons can be removed by uncommenting the `:pui_requests_permitted_for_types` line in config/config.rb and removing the record types from the set.