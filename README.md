# Hologram Demo Quick Tips

* Navigate to the project path, then run:

```
	git clone https://github.com/trulia/hologram
	cd hologram
```

* Open up the Gemfile and add this line: `gem 'hologram’` then run:

```
	sudo gem install hologram
```

  If the following error comes up, "mkmf.rb can't find header files for ruby at /usr/lib/ruby/ include/ruby.h … failed..." try this first:

```
	gcc --version
```

  Once prompted to install developer tools, click “install” and this should resolve it, then try this again:

```
sudo gem install hologram
```

* Next, initialize Hologram

```
	hologram init
```

_This creates a hologram_config.yml file as well as some template files…_

* Open up the _hologram_config.yml_ file and make updates:

```
	source: ./components
  destination: ./docs
  documentation_assets: ./templates
  dependencies:
    - ./components
  index: intro
  # code_example_templates
  # code_example_renderers
```

* Rename the “doc_assets” folder to “templates”

* Remove the “code_example_templates” folder

* Add a components directory (for this demo, we’ll be housing the CSS files in here):

* Then START DOCUMENTING your css! Keep in mind that code gets rendered twice (first as rendered code and secondly as an 'escaped' code block).

* Take a look at the files in the components folder. These are the documented css files. Feel free to clear this and add your own.

* Once you have documented the CSS files, run the following to see your generated code:

```
	hologram hologram_config.yml
```
