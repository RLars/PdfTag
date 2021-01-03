# PDFTag
PDF tag (keyword) management desktop application

# Dependencies
* libimage-exiftool-perl for PDF metadata modification
* This software uses std::filesystem, so a gcc with C++17 support shall be used.
* find
* wc
* cp


# TODO
## Table handling
* Don't lose selection on filter change as long as the selected item is available in the current filter
* Support multi-select: gtk_tree_selection_get_selected_rows

## Filtering
* Update Tag-filter list in case AvailableTags changes (new tag added, tag removed from all files)
* Date-based filter
* Improve filtering: Can we just deactivate entries in table? (gtk_tree_model_filter_set_visible_func ?)
* Sorted tag list
* search query in tag list
* only display <untagged> in case there are actually untagged PDFs?
* Add selector for AND/OR combination of tags

## Other
* Integrate into deb package management to resolve dependencies and make installation easy
* Port to gtkmm

# Issues
* Make it visible to user that a tag was not applied
* Bad performance on loading: Maybe only call exiftool once per PDF?
