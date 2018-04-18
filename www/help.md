<!--Slidoc: strip=chapters -->

# [Qwheel](https://mitotic.github.io/Qwheel): Question wheel

![screenshot](img/screenshot.png '.float-right width=20%')

A common problem facing teachers is that if you pose a question to a
class, the same few students, usually in the first row, answer
them. These students are typically not representative of the class,
being more advanced and/or paying attention. To get around this
problem, [Qwheel](https://mitotic.github.io/Qwheel) uses a spinning
*prize wheel* image (+sound) to randomly select a name from a
list. Once a name is selected, it is removed from the list (although
this behavior is optional). Using [Qwheel](https://mitotic.github.io/Qwheel) is a great way to
fairly distribute questions in the class, get to know the names of
your students, and keep them attentive.

This document provides information on how to use `Qwheel`, which is
located at the URL https://mitotic.github.io/wheel

## Setup

No accounts or logins required! Create a list of names
from the class roster and enter in the dialog box when requested.

- You can use full names, or an abbreviated form,
such as first name plus enough letters from the last name to make it
unique, e.g., ``JaneDo; JohnS``.

- Names in the list may be separated by line-breaks, semicolons,
commas or spaces.

- You can create a line-break-separated list of names by simply
copying from an Excel spreadsheet column, or from a file with a name
in each line, and pasting it into the dialog box when requested.

- The *Export* option in the drop-down menu may be used to generate an
URL that can be copied to re-create the name list in a different
browser. (To use Qwheel without accessing the web, see *Code* info
below.)

## Usage

Click on `SPIN` to rotate the wheel:

- When a name is selected, a dialog box will appear.
- Clicking `OK` will remove the selected name from the list, clicking `Cancel` will retain the name.

## Sessions

A sequence of spins starting with a new list of names
is referred to as a *session*.
- The default session has a blank name.
- Alternate session names are specified using the optional
``session`` parameter in the URL and persist indefinitely in the
browser (using information stored in browser's offline local
storage).
- The drop-down menu may be used to switch between sessions or
create a new session.
- *Restarting* a session will restore the
original list of names.
- *Deleting* a session will erase it from
the browser. (Deleting the default session will re-create it.)
- *Exporting* a session displays an URL that can be copied and
pasted in a different browser.

## Creating URLs

As an alternative to copying/pasting names, you
can generate a permanent URL for creating a new session.

- Start with a
list of semicolon- or comma-separated names.
- If there are any spaces
within names, replace them with plus (+) signs.
- Then generate a URL
string that looks like this:

[https://mitotic.github.io/wheel/?session=math101&names=Jane+Doe;John+Doe;John+Smith](https://mitotic.github.io/wheel/?session=math101&names=Jane+Doe;John+Doe;John+Smith)

You can click on the above URL to see what it does.
You can also store this URL as a hyperlink in a document and reuse it to restart a session, as
needed.
- Note that the query symbol (``?``) denotes the start of
the parameter list and the ampersand (``&``) separates
different parameters.
- The optional ``session`` parameter enables
multiple parallel sessions.
- Another optional parameter ``max``
may be used to specify the maximum number of names displayed (default:
30). If there are more names than this maximum, a random subset of
consecutive names from the list is pre-selected and displayed in the
wheel.
- If the ``names`` parameter is omitted, the list of names
can be entered manually via a dialog box.

## Sample URLs

Click on the URLs below to see them in action.

- *Enter names via dialog box for default session*:

  - [https://mitotic.github.io/wheel/](https://mitotic.github.io/wheel/)

- *Default session, comma-separated first names+last initials*: 

  - [https://mitotic.github.io/wheel/?names=JohnS,JaneD](https://mitotic.github.io/wheel/?names=JohnS,JaneD)

- *Named session, semicolon-separated names, max. display of 15 names*:

  - [https://mitotic.github.io/wheel/?session=calc101&max=15&names=John+Smith,
jr.;Jane+Doe](https://mitotic.github.io/wheel/?session=calc101&max=15&names=John+Smith,jr.;Jane+Doe)


## Code

The source code is available on [Github](https://github.com/mitotic/Qwheel). You can
download the code and open the file ``www/index.html`` in your browser
to run Qwheel locally, *even without an internet connection*, by appending
parameters to the file URL (``file:///.../index.html?names=...``).

To customize, modify the ``www/index.html`` file.  
[Qwheel](https://mitotic.github.io/Qwheel) uses the jQuery
[rouletteWheel](https://github.com/JavoByte/rouletteWheel) software for
the graphics.

## Additional tips

- Reloading the page helps if the wheel does not appear. 
- The maximum length of an URL is about 2000 characters. If names are
shortened to about 10 characters each, a maximum of about 200 names
can be handled in the URL. For a longer list, pasting into the dialog
box should work.
- If you want Qwheel to display a full name upon selection, but a
shorter name on the wheel, then use the syntax
``shortname/fullname`` for each name in the URL.
- Specify ``reset=1`` in the URL to clear all sessions. 
- An undocumented parameter ``stats=1`` can be specified to verify 
the randomness of the selection algorithm. 

*Note: This document is created from
[Markdown](https://daringfireball.net/projects/markdown/) text using
[Slidoc](https://mitotic.github.io/slidoc), a sister project of
[Qwheel](https://mitotic.github.io/Qwheel). To view it as a slide show, press the ESCAPE key.*
