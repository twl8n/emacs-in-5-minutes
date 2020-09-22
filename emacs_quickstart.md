title:Emacs key commands for beginners
keywords:emacs,keys,commands,control,escape,beginner,learn,easy,fun,powerful,
description:Quick notes on how to learn and use Emacs in less than five minutes.



Table of contents
-----------------
- What is Emacs?
- Introduction to Emacs keys
- Review
- Seven keys you need to start
- Minibuffer
- Get my .emacs (dot-emacs) init file
- Other key bindings



What is Emacs?
--------------

Emacs is a powerful tool often used for the simple task of editing
text files. Emacs is an Integrated Development Environment (IDE) which
supports many programming languages and file types. Emacs can edit,
compile, run, debug, and document. Beginners can get started with
Emacs in a few minutes, learning only seven commands. Experienced
programmers will be using Emacs decades later because it is one of the
most useful software packages ever created.

Steve Yegge sums it up in the sixth paragraph down at:

http://steve.yegge.googlepages.com/effective-emacs

Yegge says:

"Compared to Emacs Wizards, graphical-IDE users are the equivalent of
amateur musicians, pawing at their instrument with a sort of
desperation. An IDE has blinking lights and pretty dialogs that you
can't interact with properly (see Item 6), and gives newbies a nice
comfortable sense of control. But that control is extremely crude, and
all serious programmers prefer something that gives them more power."

Emacs is a complex tool, but I think my introduction and hints will
make it easy to get started. 



Introduction to Emacs keys
--------------------------

There are only 7 keyboard commands necessary to use Emacs effectively.

Using emacs requires use of the control and escape keys.
In the notes below, this is how these keys are denoted:

C		Control key, Ctrl
ESC		Escape key, Esc, also called the "meta" key

For example, C-x means hold down the control key and the x key, then
release both keys. Multiple keystrokes are separated by a space. C-x s
means do C-x as above, release both keys, then press s and release.

The Esc key is known as "meta" or "the escape key". ESC-x
means press ESC and release, then press x and release. M-x has the
same meaning.

The space bar is called spc or SPC. The enter key is RET (historically
known as the return key).

The action of a key is called the "binding". 

Use C-g to cancel any running command or any multi-key operation.



Review
------

C-x is press Ctrl and x, then release both keys.

C-x s is press Ctrl and x, release both, then press s and release.

M-x is press Esc and release, then press x and release.

C-g is press Ctrl and g, then release both keys. Use C-g to cancel.



Seven keys you need to start
----------------------------

key             binding
---             -------

Cancel:
C-g		keyboard-quit (cancel)

Open file:
C-x f		find-file (open file)

Save:
C-x s		save-buffer (save)

Save and exit
C-x C-c		save-buffers-kill-emacs (exit, quit)

Cut:
mark, move cursor, cut
C-SPC, move cursor, C-w

Copy:
mark, move cursor, copy
C-SPC, move cursor, ESC-w

Paste:
C-y		yank (paste)

Use the cursor control keys (arrows), page-up, page-down, home, and
end to navigate (that is: to move the cursor). Running Emacs in a
graphical environment allows you to use the mouse. You can use emacs
with just these simple keys.

Emacs has many other wonderful features. Keyboard macros automate
repetitive actions. Compile will compile your code without leaving
emacs, and when there are errors, you can jump to the offending line
of code. Splitting the screen enables you to look at two (or more)
files, or two parts of the same file. Marking (selecting) a block of
code and using comment-region (M-#) will comment out a region of
code. The list is huge. M-x tab lists 2453 commands in the Completions
window.




Minibuffer
----------

The line at the bottom of the screen is the minibuffer. Emacs sends
you messages here. You enter commands here via the M-x command. When
you open a file, the file name appears in the minibuffer. If you try
to exit with unsaved buffers, emacs will ask if you are sure, and if
you want to save each file. Some questions expect y or n answers, and
others require a yes or no.



Get my .emacs (dot-emacs) init file
-----------------------------------

You should get my .emacs (pronounced "dot emacs") file and save it in
your home directory. My .emacs contains improved key bindings and many
useful additions. You can modify the .emacs file, and move it onto all
systems where you work.

http://defindit.com/readme_files/tom_emacs.txt

Linux and OSX: download to your home directory and rename to .emacs

Windows: probably put in C:\ and name _emacs (with a leading underscore) or .emacs and see the
documentation "Where do I put my init file" at:

http://www.gnu.org/software/emacs/windows/Installing-Emacs.html

On Linux and OSX, use your favorite package manager (yum, yast, etc.)
to install Emacs. It has a huge amount of functionality, and is
therefore fairly large (70 MB). The full Emacs install may consist of 3
packages: emacs, emacs-common, and emacs-release.

For Windows, download the single binary from the GNU ftp site. Unzip
in a logical location (program files). Most people want the full "bin"
which are all binaries and docs (no source).

http://ftp.gnu.org/gnu/emacs/windows/

For example:

http://ftp.gnu.org/gnu/emacs/windows/emacs-22.3-bin-i386.zip



Other key bindings
------------------

The keys above are the minimal commands necessary to use emacs,
assuming you use the use the keyboard arrow keys to move the
cursor. Below is a more-or-less complete list of bindings.

The M-x binding is speaicl. When you do M-x the text "M-x " will
appear in the "mini-buffer" at the bottom of the emacs screen. M-x is
the Emacs "command mode". M-x expects you to enter a command, then
press the Enter (return) key to run the command. Commands will
auto-complete if you press the spacebar.

Holding down the Alt key and pressing a second key (the release both
keys) behaves as though you pressed ESC, released it, then pressed a
second key. For example, "press and hold Alt, then press x, then
release both" is identical to "press and release ESC, press and
release x". The Alt shortcut is handy for certain scrolling commands.


key             binding
---             -------

C-x		Control-x, the Prefix Command (see use below)

Cursor moving:
Use arrow keys or:
C-b		backward-char (move cursor left)
C-f		forward-char (move cursor right)
C-n		next-line (cursor down)
C-p		previous-line (cursor up)
C-a		beginning-of-line (move cursor)
C-e		end-of-line (move cursor)
Alt-n		up-one (scroll page up one line without moving the cursor)
Alt-p		down-one (scroll page down one line without moving the cusor)

Search:
C-s		search-forward
ESC-ESC		repeat-complex-command (repeat last search)



Commands below are extra emacs features, and some review of the 
information above.

C-x C-z		suspend emacs (background emacs, return to shell.
		use "fg" to foreground emacs)

Compile/syntax check Perl:
C-x c  then delete text in minibuffer and
replace with "perl -cw filename.pl" and press Enter/Return to begin compiling.

C-x c		compile
C-x C-n		next-error (go to next error shown in compile results)
ESC g		goto-line

C-w		kill-region (cut)
C-y		yank (paste)
C-x C-c		save-buffers-kill-emacs (exit, quit)
C-x f		find-file (open file)
C-x C-f		find-file (open file)
C-x C-r		find-file-read-only (open read-only)
C-x s		save-buffer (save)
C-x C-s		save-buffer (save)
C-x C-w		write-file (save-as)
ESC w		append-next-kill (copy)

C-SPC		set-mark-command (mark start of cut/copy)
C-a		beginning-of-line (move cursor home)
C-b		backward-char (move cursor left)
C-d		delete-char (delete character at current position, e.g. delete forward)
C-e		end-of-line (move cursor)
C-f		forward-char (move cursor right)
C-g		keyboard-quit (cancel)
C-h		backward-delete-char (backspace)
C-k		kill-line (delete line)
C-l		recenter (redraw screen)
RET		newline
C-n		next-line (cursor down)
C-o		open-line (insert blank line)
C-p		previous-line (cursor up)
C-q		quoted-insert
C-r		search-backward
C-s		search-forward
M-z		scroll-up (page down. By Emacs tradition C-v, but that mean "paste" to everyone else.)
M-a		page up
C-w		kill-region (cut)
C-x		Control-X-prefix
C-y		yank (paste)
M-n		up-one (Alt-n Emacs Alt is somewhat like a shift/control Meta key.)
M-p		down-one (Alt-p Emacs Alt is somewhat like a shift/control Meta key.)

C-_		undo (control-shift-underscore)

C-x C-b		list-buffers
C-x C-c		save-buffers-kill-emacs (exit, quit)
C-x C-d		list-directory
C-x f		find-file (open file)
C-x C-r		find-file-read-only (open read-only)
C-x s		save-buffer (save)

C-x C-w		write-file (save-as)
C-x C-x		exchange-point-and-mark (move cursor to mark location)

C-x (		start-kbd-macro
C-x )		end-kbd-macro
C-x e		call-last-kbd-macro (run macro)

C-x n		other-window (when screen is split, switch to other window)
C-x 1		delete-other-windows (unsplit window, make one one window)
C-x 2		split-window-vertically (split screen into two windows)

C-x =		what-cursor-position

C-x b		switch-to-buffer
C-x c		compile
C-x C-n		next-error

C-x f		find-file (open file)

C-x k		kill-buffer (close file)

ESC w		append-next-kill (copy)
ESC ESC		repeat-complex-command
ESC g		goto-line

Useful commands to try via M-x
------------------------------

Remember, emacs will auto complete commands. Begin typing, the press
tab to see a list of commands. You may want to press tab twice. 

I never type the command:

M-x describe-key-briefly

Instead I type:

M-x desc TAB k TAB - TAB return

apropos (search Emacs function and variable descriptions)
manual-entry (open a man page)
toggle-read-only (toggle a buffer between read-only and read-write)
describe-key-briefly (describe a keystroke command)
desecribe-bindings (list all current commands which have keystrokes)
