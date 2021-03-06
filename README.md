#  Roundarch Isobar Front-end Development Standards and Guidelines [http://isobar-idev.github.com/code-standards](http://isobar-idev.github.com/code-standards)

## License:

All content licensed under Creative Commons Attribution 3.0 Unported License

## Branch Updates

Update: 1/28/13 - The vast majority of the merge issues have been resolved at this point, save for some changes we have coming from a private repository. In the process of removing the PHP files as well as we're fully migrating to Github hosted pages. A Grunt.js build process is on the way as well as a mobile/responsive layout. Keep your eyes open and touch base if you'd like to help! We have several issues open in the issue tracker.

## Please Update Your Bookmarks

It is important that anyone who follows these standards note that as of mid-September 2012, the [old link](http://na.isobar.com/standards) has been retired in favor of the new Github-hosted version of the documents. 

> **New Link:** [Roundarch Isobar Front End Code Standards & Guidelines](http://isobar-idev.github.com/code-standards)

The Roundarch Isobar Front End Code Standards & Guidelines document is a living document that has many changes on the way. We're also going to be making some subtle changes to the Github repo structure so please keep your eyes open.

## Master Branch Madness

There was an errant series of commits to the master branch of this repo earlier this year, which resulted in the HTML5 Boilerplate history being brought into the repo.

Due to the extent of the issues and subsequent conflicts in trying to rebase based on prior commits, we opted for the extreme measure of replacing/renaming the `master` branch on this repo.

> Apologies in advance. This may result in some FORKS or local CLONES looking woefully out of date (in the order of 300 commits). The best thing for users to do is to fork again, rebase, or just start with a fresh master locally.

## Summary:

This document contains guidelines for web applications built by the Creative Technology (front end engineering) practice of Roundarch Isobar (previously Isobar & Molecular). It is to be readily available to anyone who wishes to check or contribute to the iterative progress of our discipline's best practices.

This document's primary motivation is two- fold: 1) code consistency and 2) best practices. By maintaining consistency in coding styles and conventions, we can ease the burden of legacy code maintenance, and mitigate risk of breakage in the future. By adhering to best practices, we ensure optimized page loading, performance and maintainable code.

Code standards are living documents, and should themselves change to reflect the latest best practices, thought leadership, and trends both in the community whose practices they seek to standardize and in the greater development community as a whole. Front-end development is one of the fastest growing disciplines in software development; to ensure that our standards are able to keep pace, we want you to fork us, discuss additions, send us pull requests, and add issues to debate emerging standards and practices.

We hope to encourage other developers to think about how to best standardize their approaches to development, to propose their own ideas for debate and for inclusion in our version of the document, and to adapt our standards for their own unique development practices. What better way of achieving consensus on how best to develop in our discipline than through feedback from members of that discipline themselves?

## Structure of Page Content

The index.html file is generated via grunt, including each of the .html files contained within the /sections/[lang] directory. We have separated the different sections that make up the page into individual files so that it is easier to edit, basically making the content of the page more modular. This is also part of what we consider a best practice when dealing with large projects, as if it were an application involving lots of code, that several people work on. index.html is then served via jekyll using the layout located in _layouts/main.html.

Each of these files include content wrapped within sections. This should be self-explanatory I think. In each section, we make use of all h1-h6 heading tags multiple times since HTML5 lets you use as many as you like. Of course, we try to always use them and all other HTML5 tags appropriately, and making use of semantic tags where they are best suited.

To edit the main layout, edit the file in _layouts/main.html, to edit the content edit the relevant section in the sections folder. Do not edit index.html.

## Structure of CSS

The CSS files are generated via compass from the scss files located in the scss folder, which is run as part of the grunt task. Because github pages only serve static content, you must push your generated files to the gh-pages branch for updates to appear. 

## Getting Started with the Build process

Prior to running these commands, make sure you have ruby 1.9.3 installed, ideally using RVM.

Run 'npm install' from the command line of the project directory to install all the node dependencies. You may need to occasionally re-run this command as new dependencies are added.

Run 'bundle install' from the command line of the project directory to install ruby's dependencies. This will allow you to build the jekyll site similiar to what we are hosting on github pages, and to run the server locally. If you get a 'command not found' error, run 'gem install bundler' then try again.

Run 'grunt' from the command line of the project directory to run the build process.

To run the jekyll server locally run 'jekyll serve --watch' from the command line. You can then view the site at localhost:4000. Don't forget the '--watch' option as this enables auto-regeneration of the code.

We currently use the default jekyll configuration, so there is no configuration file.


