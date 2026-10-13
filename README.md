**ReadMe Document**

*The below changes were made to fix the above application*

## Changes Made

| Feature | Issue | Fix Implemented |
|---|---|---|
| Genre Dropdown | The dropdown used `title` as its selected value instead of `genre`. | Changed `selectedValue={title}` to `selectedValue={genre}`. |
| Genre Selection | Each genre option used `value={genre}`, causing incorrect selection values. | Changed to `value={item}` so each option saves its correct genre. |
| Adding Albums | Adding a new album replaced the existing collection. | Used `setAlbums((currentAlbums) => [...currentAlbums, temporaryAlbum])` to preserve existing albums. |
| Deleting Albums | The delete function kept the selected album instead of removing it. | Changed the filter condition from `=== id` to `!== id`. |
| FlatList Keys | Album titles were used as keys, which could cause duplicate-key issues. | Changed `keyExtractor` to use the unique album `id`. |
| Year Validation | Future release years were not rejected. | Added validation to ensure the year is between 1900 and the current year. |
| Rating Validation | The upper rating limit was not explicitly checked. | Added validation to ensure ratings are whole numbers between 1 and 5. |
