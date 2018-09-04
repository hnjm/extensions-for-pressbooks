# User Manual

## Introduction

This manual gives brief explainations on features of the plugin, which could be useful for developement of your website and for understanding how to recieve desired behaviour of a plugin.

## Edition 

Edition extension simply creates new field in `Book Info` page in `General Book Info` metabox and works in the same way as the other fields in that page.


## Original Mark

Original Mark package provides network administrators with ability to mark books of original publisher. It is done with a checkbox in `/wp-admin/network/sites.php` page, after activation of a plugin you will have new column there with name 'Featured Books'.

## Translations relations

In case you are creating translations of your books, 'Translations relations' can help you with automatic linking between all of the the translations and original book. For current moment plugin logically interconnects only books about languages.

### Adding new translations

**Read carefully the following instructions and follow them one by one, otherwise it can lead to incorrect working result of a plugin!** The working steps to create relations between you books are following:

1. With use of `Original Mark` tick the checkbox in `/wp-admin/network/sites.php` `Featured Book` column in front of book in original language. *Wait until notification!*
1. Go to `Book Info` page of a book which is a translation (this book **must** be created with `Cloning Tool` using original book as a source), allocate `Studying Content` metabox (if book was not cloned, this metabox will not be shown) and choose which language is this book about.
	* In case the book is not actually a translation, but just a modification, choose 'Not translation' option in that metabox in order too keep consistenty of translations interactions.
1. On the same page choose language of a book in `General Book Information` metabox, if it was not done before.
1. Update Book Info.
1. Go back to `/wp-admin/network/sites.php` page and mark translated book as `Featured Book`. *Wait until notification!*

For more translations repeat steps from 2 to 5 in the list above.

### Deleting translations

In order to delete book from relational system, just simply unmark `Featured Book` checkbox in `/wp-admin/network/sites.php` in front of that book.

If you would like to drop all the relations of series of book and its translations, unmark `Featured Book` checkbox in `/wp-admin/network/sites.php` in front of original book. *Be careful!* After this all the translation will also be unmarked as featured books.

### Changing language of translated book

If by mistake you have put the wrong language of a book in point 3 of working steps and you would like to change it to a correct one, in order to keep the consistent relations do following:
1. Go to `/wp-admin/network/sites.php` and unmark translated book in `Featured Book` column. *Wait until notification!*
1. Go to `Book Info` page of that book, change language of a book to a desired one in `General Book Information` metabox.
1. Go back to `/wp-admin/network/sites.php` page and mark translated book as `Featured Book`. *Wait until notification!*

### Printing links in web-pages

In order for the links to be shown in the front-end of a website, use our [theme](https://github.com/my-language-skills/books4languages-book-child-theme-for-pressbooks). Since some relations will be established, the links will appear in the footer of every web-page of your connected books. **Note!** Do not change permalinks in your translations, otherwise links will lead to non-existing pages in other books. 