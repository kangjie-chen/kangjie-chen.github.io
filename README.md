A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

I think I've got things running smoothly and fixed some major bugs, but feel free to file issues or make pull requests if you want to improve the generic template / theme.

### Note: if you are using this repo and now get a notification about a security vulnerability, delete the Gemfile.lock file. 

# Instructions

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
1. Set site-wide configuration and create content & metadata (see below -- also see [this set of diffs](http://archive.is/3TPas) showing what files were changed to set up [an example site](https://getorg-testacct.github.io) for a user with the username "getorg-testacct")
1. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
1. Check status by going to the repository settings, in the "GitHub pages" section
1. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/


## To run locally on Windows (not on GitHub Pages, to serve on your own computer)
[Github Docs](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)

1. Clone the repository and made updates as detailed above
2. Install Ruby and Ruby DevKit from https://rubyinstaller.org/downloads/
3. *run the following commands in the windows-terminal*, not the vscode terminal. I do not know why this is necessary.
3. Install Jekyll and Bundler by running `gem install jekyll` in a command prompt
4. Run `bundle clean` to clean up the directory (no need to run `--force`) 
5. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
6. Run `bundle exec jekyll liveserve -o` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change. (-o means open pages automatically)

Some errors you might get:
- Error:  No source of timezone data could be found. 
[add "gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw]" into Gemfile in the root folder of this project](https://github.com/tzinfo/tzinfo/wiki/Resolving-TZInfo::DataSourceNotFound-Errors)

- Error: /Ruby31-x64/lib/ruby/gems/3.1.0/gems/hawkins-2.0.5/lib/hawkins/servlet.rb:1:in 'require': cannot load such file -- webrick (LoadError) [`bundle add webrick`](https://github.com/jekyll/jekyll/issues/8523)



## To run locally on Linux (not on GitHub Pages, to serve on your own computer)
[Docs on academicpages.github.io](https://academicpages.github.io/)



