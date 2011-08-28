PDV (phpDocumentor for Vim)
===========================

Version: 1.0.1

Copyright 2005 by Tobias Schlitt <toby@php.net>
Inspired by phpDoc script for Vim by Vidyut Luther (http://www.phpcult.com/).

Provided under the GPL (http://www.gnu.org/copyleft/gpl.html).

This script provides functions to generate phpDocumentor conform
documentation blocks for your PHP code. The script currently
documents:

- Classes
- Methods/Functions
- Attributes

All of those supporting all PHP 4 and 5 syntax elements. 

Beside that it allows you to define default values for phpDocumentor tags 
like @version (I use $id$ here), @author, @license and so on. 

For function/method parameters and attributes, the script tries to guess the 
type as good as possible from PHP5 type hints or default values (array, bool, 
int, string...).

You can use this script by mapping the function PhpDoc() to any
key combination. Hit this on the line where the element to document
resides and the doc block will be created directly above that line.

Installation
============

For example include into your .vimrc:

source ~/.vim/php-doc.vim
imap <C-o> set paste<CR>:exe PhpDoc()<CR>:set nopaste<CR>i

This includes the script and maps the combination <ctrl>+o (only in
insert mode) to the doc function. 

