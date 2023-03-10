Samba is a free SMB and CIFS client and server and Domain Controller for UNIX
and other operating systems. It is maintained by the Samba Team, who support the
original author, Andrew Tridgell.

This software is freely distributable under the GNU public license, a copy of
which you should have received with this software (in a file called COPYING).

# WHAT IS SMB/CIFS?
This is a big question.

The very short answer is that it is the protocol by which a lot of PC-related
machines share files and printers and other information such as lists of
available files and printers. Operating systems that support this natively
include Windows 9x, Windows NT (and derivatives), OS/2, Mac OS X and Linux. Add
on packages that achieve the same thing are available for DOS, Windows 3.1, VMS,
Unix of all kinds, MVS, and more.  Some Web Browsers can speak this protocol as
well (smb://).  Alternatives to SMB include Netware, NFS, Appletalk, Banyan
Vines, Decnet etc; many of these have advantages but none are both public
specifications and widely implemented in desktop machines by default.

The Common Internet File system (CIFS) is what the new SMB initiative is called.
For details watch [here](https://samba.org/cifs)

# WHY DO PEOPLE WANT TO USE SMB?
* Many people want to integrate their Microsoft desktop clients with their Unix
servers.

* Others want to integrate their Microsoft (etc) servers with Unix servers. This
is a different problem to integrating desktop clients.

* Others want to replace protocols like NFS, DecNet and Novell NCP, especially
when used with PCs.

# WHAT CAN SAMBA DO?
Please refer to the WHATSNEW.txt included with this README for a list of
features in the latest Samba release.

Here is a very short list of what samba includes, and what it does. For many
networks this can be simply summarized by "Samba provides a complete replacement
for Windows NT, Warp, NFS or Netware servers."
* a SMB server, to provide Windows NT and LAN Manager-style file and print
services to SMB clients such as Windows 95, Warp Server, smbfs and others.

* a Windows Domain Controller (NT4 and AD) replacement.

* a file/print server that can act as a member of a Windows NT 4.0 or Active
Directory domain.

* a NetBIOS (rfc1001/1002) nameserver, which amongst other things gives browsing
support. Samba can be the master browser on your LAN if you wish.

* a ftp-like SMB client so you can access PC resources (disks and printers) from
UNIX, Netware, and other operating systems

* a tar extension to the client for backing up PCs

* limited command-line tool that supports some of the NT administrative
functionality, which can be used on Samba, NT workstation and NT server.

For a much better overview have a look at the [web site](http://samba.org/samba)
and browse the user survey.

#### Related packages include:
* cifsvfs, an advanced Linux-only filesystem allowing you to mount remote SMB
filesystems from PCs on your Linux box. This is included as standard with Linux
2.5 and later.

* smbfs, the previous Linux-only filesystem allowing you to mount remote SMB
filesystems from PCs on your Linux box. This is included as standard with Linux
2.0 and later.

# CONTRIBUTIONS

### To contribute via GitHub
  * fork the official Samba team repository on GitHub
    -- see [GitHub](https://github.com/samba-team/samba)

  * become familiar with the coding standards as described in README.Coding

  * make sure you read the Samba copyright policy
    -- see [Copyright Policy](https://www.samba.org/samba/devel/copyright-policy.html)

  * create a feature branch

  * make changes

  * when committing, be sure to add signed-off-by tags
    -- see [Commit message tags](https://wiki.samba.org/index.php/CodeReview#commit_message_tags)

  * send a pull request for your branch through GitHub

  * this will trigger an email to the samba-technical mailing list

  * discussion happens on the samba-technical mailing list as described below

  * more info on using Git for Samba development can be found on Samba Wiki
    -- see [Using Git for Samba](https://wiki.samba.org/index.php/Using_Git_for_Samba_Development)

### To contribute via mailing lists
Join the mailing list. The Samba team accepts patches (preferably in "diff -u"
format, see [here](https://samba.org/samba/devel) for more details) and are
always glad to receive feedback or suggestions to the address
samba@lists.samba.org. More information on the various Samba mailing lists can
be found at [mailman](http://lists.samba.org).

You can also get the Samba sourcecode straight from the [git repository](http://wiki.samba.org/index.php/Using_Git_for_Samba_Development).

If you like a particular feature then look through the git change-log on the
[web](https://git.samba.org/?p=samba.git;a=summary) and see who added it, then
send them an email.

Remember that free software of this kind lives or dies by the response we get.
If no one tells us they like it then we'll probably move onto something else.


# MORE INFO

### DOCUMENTATION
There is quite a bit of documentation included with the package, including man
pages, and lots of .html files with hints and useful info. This is also
available from the web page. There is a growing collection of information under
docs/.

A list of Samba documentation in languages other than English is available on
the web page.

If you would like to help with the documentation, please coordinate on the
samba@lists.samba.org mailing list. See the next section for details on
subscribing to samba mailing lists.

### MAILING LIST
Please do NOT send subscription/unsubscription requests to the lists!

There is a mailing list for discussion of Samba.  For details go to [mailman](https://lists.samba.org)
or send mail to <samba-subscribe@lists.samba.org>.

There is also an announcement mailing list where new versions are announced. To
subscribe go to [mailman](http://lists.samba.org) or send mail to
<samba-announce-subscribe@lists.samba.org>. All announcements also go to the
samba list, so you only need to be on one.

For details of other Samba mailing lists and for access to archives, see
[mailman](http://lists.samba.org)

### MAILING LIST ETIQUETTE

A few tips when submitting to this or any mailing list.
 - Make your subject short and descriptive. Avoid the words "help" or "Samba" in
the subject. The readers of this list already know that a) you need help, and b)
you are writing about samba (of course, you may need to distinguish between
Samba PDC and other file sharing software). Avoid phrases such as "what is" and
"how do i". Some good subject lines might look like "Slow response with Excel
files" or "Migrating from Samba PDC to NT PDC".

- If you include the original message in your reply, trim it so that only the
relevant lines, enough to establish context, are included. Chances are (since
this is a mailing list) we've already read the original message.

- Trim irrelevant headers from the original message in your reply. All we need
to see is a) From, b) Date, and c) Subject. We don't even really need the
Subject, if you haven't changed it. Better yet is to just preface the original
message with "On [date] [someone] wrote:".

- Please don't reply to or argue about spam, spam filters or viruses on any
Samba lists. We do have a spam filtering system that is working quite well thank
you very much but occasionally unwanted messages slip through. Deal with it.

- Never say "Me too." It doesn't help anyone solve the problem. Instead, if you
ARE having the same problem, give more information. Have you seen something that
the other writer hasn't mentioned, which may be helpful?

- If you ask about a problem, then come up with the solution on your own or
through another source, by all means post it. Someone else may have the same
problem and is waiting for an answer, but never hears of it.

- Give as much *relevant* information as possible such as Samba release number,
OS, kernel version, etc...

- RTFM. Google.

### WEB SITE
A Samba WWW [site](https://samba.org) has been setup with lots of useful info.

As well as general information and documentation, this also has searchable
archives of the mailing list and a user survey that shows who else is using this
package.
