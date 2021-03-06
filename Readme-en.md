Musite
======


Introduction
------------

[Musite](https://github.com/jperon/musite) is a kind of wiki meant
chiefly for editing musical documents. It has been created, in connection
with the [Gregorio Project](https://github.com/gregorio-project),
as a way to facilitate editing works which contain both Gregorian
scores (made with [Gregorio](http://gregorio-project.github.io)) and
classical scores (made with [Lilypond](http://lilypond.org)).

From the main page, you may:

- consult the list of existing projects;
- create a new project.

From the list of projects, you may:

- clone an existing project (through `git`, the version control system
  used by musite);
- send a `zip` archive containing a project already begun elsewhere,
  which will then be made part of musite.

If you wish to have a project begun elsewhere become part of musite,
bear in mind the following:

- the project's main directory should be compressed in the `zip`
  format;
- the root of that `zip` archive must contain only the main directory;
- if that directory contains a `.git` subdirectory, the history of
  earlier changes will be available in musite; otherwise, musite will
  initialize a new `git` repository, which will record subsequent
  changes.

Musite has been translated into English by means of
[gettext](https://www.gnu.org/software/gettext); translations into
other languages are quite possible, if volunteers step forward.


Project
-------

A project's main page posts:

- the list of directories and files in the project;
- if there is a `Readme.md`, its contents, located at the project's
  root.

It is possible to have several `Readme` files, to suit speakers of
different languages: if a user navigates to the English version of the
site and a file called `Readme-en.md` exists, that file will be
served.

The menu to the left on the main page offers:

- a link to the project's page (this is useful after certain actions
  on the project);
- the different actions possible.

### Actions on a project

#### Unauthenticated user

An unauthenticated user may:

- gain read-only access to a project's history, so as to follow the
  successive changes to the project's files;
- download the project as a compressed `zip` archive.

#### Authenticated user

The actions available to an authenticated user depend on the
privileges which have been granted to that user. At present, there are
two levels of privileges:

- *administrators* can change important parameters of the site (this
  is discussed in another section of the documentation);
- *editors* can change documents and the directories within a project.

Besides the actions available to any user, here are those an editor
may perform:

- copying a project;
- creating documents or subdirectories;
- sending changes to and receiving them from a remote repository;
- inserting a file, or an archive containing files or directories,
  into a project;
- gaining read-write access to the history, so as to undo changes;
- renaming a project;
- deleting a project.

All of these actions are reversible, except for deleting a project. If
you must delete a project, remember to download it, in order to have a
back-up.

See the next section for incorporating existing files or archives.


Directory
---------

From a project's page, you may gain access to a directory by clicking
on its name. The directory's main page looks much like the project's,
with some differences:

- besides the link to the root of the project, there is a link to the
  parent directory;
- the available actions are those which make sense with directories.

Be sure to note the following points about incorporating existing
documents into musite:

- when you send a **single file**, unless you check the box marked
  *Overwrite the file if it exists*, musite will begin by protecting
  a file with the same name;
- however, when you incorporate an **archive** containing a tree
  (files and directories), musite will overwrite any existing files
  without warning. If you make a mistake, you can use musite's history
  to fix it.


Document
--------

From a project or a directory, you may gain access to various
documents. Musite adapts to a file's extension; if a file has no
extension or an extension unknown to musite, that file is treated, if
possible, as a text file. For binary files of an unknown kind, no
preview is possible, but the other actions are available.

So, if a document's kind is known, its main page is a preview of the
document; if its kind is unknown, its source is shown.

The available actions on a document are:

- for unauthenticated users, previewing it, showing its source, and
  viewing its history;
- for editors, editing, copying, moving, and deleting, as well as
  gaining read-write access to its history.

Besides all this, some kinds of document offer export to various
formats: this allows you, say, to print a score in a different format
than presented in the document's preview.


Acceptable formats
------------------

At this time, musite can handle the following formats:

- [gabc](http://gregorio-project.github.io/gabc/index.html) for
  Gregorian scores;
- [lilypond](www.lilypond.org/text-input.fr.html) for
  classical scores;
- [latex](www.latex-project.org) for typesetting publications;
- [markdown](commonmark.org) for enriched text;
- txt for text documents; any document of unknown kind can be treated
  as plain text if it is not binary.
