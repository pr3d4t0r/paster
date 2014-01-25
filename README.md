Paster
======
Paste text from the current document onto a public pastebin or board.  This
implementation is written in vim to reduce external dependencies to Python or
Perl.  The only external dependency is cURL (e.g. /usr/bin/curl in UNIX-like
systems) as an HTTP posting tool.  This posting tool, and all its command line
parameters are configurable by the user.

Features:

* Pastes to any pastebin with a public API
* The end-user's nick is configurable per use, or via .vimrc
* Sends syntax highlighting information if the target supports it
* Uses standard vim range commands for its use
* Copies the URL where the text was pasted to the system clipboard and the status line
* Opens a web browser at the page where the paste was posted (v1.2) 

Usage
=====
Install paster.vim to the appropriate default vim scripts directory for your
configuration, e.g. `$HOME/.vim/plugin`

Once installed, the Paste[bin] command may be invoked in any of these patterns:

```
:.Paste -- paste the current line
:%Paste -- paste the entire document
:42,69Paste -- paste lines 42 through 69, inclusive 
```

The Paste command will work with selections made in visual mode as well.

Paste will prompt for a value if the user hasn't defined a /nick or ID prior
to the command's first invocation.

Upon successful completion, Paste will display the URL to the paste.  Paste will also copy it to the window manager's clipboard under
MacVim and gvim. 


Installation
============

UNIX-like systems:

``` bash
cd ~/.vim

unzip /path/to/paster.zip

vi
:helptags ~/.vim/doc
```

Windows systems:

Unpack the .zip file and copy the files to your
gvim or vim configuration directory, then:

``` vim
vi
:helptags /path/to/doc
```


Caveat emptor
-------------
Unfortunately none of the developers or testers had access to a Windows
machine, so this wasn't tested in that environment.  Please let me 
know if you had issues using the URL in the next section.


Comments, questions, bug reports
--------------------------------

Eugene Ciurana, http://eugeneciurana.com/contact or http://ciurana.eu/contact
for your questions.

Project page:  http://www.github.com/pr3d4t0r/paster

Installation page:  http://www.vim.org/scripts/script.php?script_id=2602


Contributors, license, other information
----------------------------------------
Use the Force.  Read the Source.

The paster.vim source file features the contributors list and
version history.  The configuration is documented in the
paster-config.vim file.


