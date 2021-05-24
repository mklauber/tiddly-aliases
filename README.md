# tiddly-aliases
JS-based implementation of Wikipedia-style aliases and redirects for non existing tiddlers. This plugin allows you to setup tiddlers with an "aliases" field. All aliases will then also be links to the parent tiddler. This could be useful for situations where you want multiple terms to refer to the same thing, such as when a character has multiple names.

Known limitations:
* An alias does not re-render automatically when you change the number of aliases it points to. This can make links that look like they're missing actually resolve, and links that look like they resolve instead go to a disambiguation page. However, this issue only lasts until the tiddler holding the link is re-rendered.
* In TiddlyWiki 5.1.22 and below, the 'Missing tiddler' tool is populated with aliases, limiting its usefulness. This problem is corrected in versions TiddlyWiki 5.1.23 and above using the "enlist-input" function, which is available only on these more recent versions of TiddlyWiki.

How-to:
* Install from https://mklauber.github.io/tw5-plugins/ or upload files to your Tiddlywiki instance.
* To add aliases to a tiddler, create an "aliases" field and add as many aliases as you desire. For one single single-word aliases, no brackets are needed. For several aliases, use double square brackets to separate aliases (eg. [[alias1]] [[another alias]] ).

Change log:
210524: The 'Missing tiddler' tool was populated with aliases, limiting its usefulness. The problem is corrected on versions TiddlyWiki 5.1.23 and above, while behaviour is unchanged on prior versions. The problem is corrected on recent versions of TiddlyWiki by adapting the filter used in [[$:/core/Filters/Missing]] by using the "enlist-input" function, which is available only on TiddlyWiki 5.1.23 and above.
