---
layout: page
title: "Bug Upload (old tracking system) - Report a bug"
description: "This is the bug reporting page for the old tracking system. If possible please use the new tracking system on GitHub instead."
---


> This is the upload page for the old bug tracking for LaTeX2e that we wish to retire.
>
> For the time being it is also still possible to open a bug report in
> the old system but we would
> appreciate if you use the new tracking system instead:
>
>  - [Issue Tracker for LaTeX2e](https://github.com/latex3/latex2e/issues)
>
> To open a bug report with the new tracking system go to the above link click on "New Issue"
> there and fill out the necessary information in the form  -- thanks.


# Instructions for the old (obsolete) tracking system

## Before submitting a LaTeX bug

A few important preparation steps to go through:

 1. **Check to see if the bug has already been
    reported.** You can do this by searching
    the <a href="{{site.baseurl}}/cgi-bin/ltxbugs2html?introduction=yes&amp;state=open">LaTeX
    bugs database</a>. If the bug has already been reported then there
    may be a documented workaround for your problem.
 1. **Check that there really is a bug**, by writing a
    short, self-contained document that shows the problem. This file should start with the line
    [`\RequirePackage{latexbug}`](https://raw.githubusercontent.com/latex3/latexbug/master/latexbug.sty). Starting with
    this package will help you to
    make sure that the document doesn't use any third-party packages or
    document classes. If the bug turns out to be with third-party
    software then please contact the developer, and not us!
 1. **For bugs related to LaTeX3 code** (expl3, xparse
    and so on): Do not report the bug here but instead use
    the <a href="https://github.com/latex3/latex3/issues">GitHub
    issue tracker</a>.
 1. **Run LaTeX on the test file.** Send the test file
    and the resulting transcript file using the form below.

Now you are ready to submit a LaTeX bug report.

> But please remember: Bug reports sent to us without a
> [`\RequirePackage{latexbug}`](https://raw.githubusercontent.com/latex3/latexbug/master/latexbug.sty) line and/or
> containing third-party code flagged by the [`latexbug`](https://raw.githubusercontent.com/latex3/latexbug/master/latexbug.sty)
> package are likely to be closed without any
> comment in our bug tracking system!




## Submit a LaTeX bug

<form action="{{site.baseurl}}/cgi-bin/latex-bugs-upload.cgi" method="POST" enctype="multipart/form-data">
  <ol>
    <li>
      <p><strong>Please add a few bits of information that will help us to categorize it.</strong> We need at least the bug category, your name, your email, and a summary (typically one sentence).</p>
      <p>LaTeX Bug category:<br>
        <select name="Category">
           <option value="amslatex">AMS LaTeX</option>
           <option value="babel">Babel</option>
           <option value="graphics">Graphics and color</option>
           <option selected value="latex">LaTeX</option>
          <!-- <option value="mfnfss">Metafont fonts</option> -->
           <option value="psnfss">PostScript fonts</option>
           <option value="cyrillic">Support for Cyrillic encodings</option>
           <option value="tools">Tools</option>
        </select>
      </p>
      <p>Class of bug:<br>
        <select name="Class">
         <option selected value="sw-bug">Software Problem</option>
         <option value="doc-bug">Documentation Problem</option>
         <option value="change-request">Change Request</option>
        </select>
      </p>
      <p>Your name:<br>
        <input type="TEXT" name="name" size="60">
      </p>
      <p>Your email:<br>
        <input type="TEXT" name="email" size="60">
      </p>
      <p>One-line summary description:<br>
        <input type="TEXT" name="summary" size="60">
      </p>
      <p>Short problem description:<br>
        <textarea name="description" rows="6" cols="60" wrap="PHYSICAL"></textarea>
      </p>
    </li>
    <li>
      <p><strong>Add the name of your input file on your computer (the button pops up a file selection box, or just type it in).</strong> It will be
  uploaded when you submit this form in step (4).<br>
        <input type="FILE" name="texfile" size="40">
      </p>
    </li>
    <li>
      <p><strong>Add the name of your transcript (log) file on your computer (the button pops up a file selection box, or just type it in).  Do not submit  your output (e.g., dvi or pdf) file here!</strong> It will be uploaded when you submit this form in step (4).<br>
        <input type="FILE" name="logfile" size="40">
      </p>
    </li>
    <li>
      <p><strong>A simple answer to prove that you are a human and not a SPAMBot.</strong> We had a lot of SPAM coming through this web form, so we ask you to in type in a number in answer to a simple question.<br> What is the sum of five hundred seventeen and four?<br>
        <input type="TEXT" name="sum" size="60">
      </p>
    </li>
    <li>
      <p><strong>Thanks for providing the information &ndash; and thanks for your contribution.</strong> You keep LaTeX going!<br>
        <input type="SUBMIT" value="Submit">
        <input type="RESET" name="">
      </p>
    </li>
  </ol>
</form>
